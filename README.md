



<h1 align="center"> Seu título aqui </h1>



##### 1) Definição
  
   <p>  Link Jsoncrack  <a href="https://jsoncrack.com/editor">jsoncrack</a></p>

```json
[{"atualizacaoPagamentosJob":[[{"ultimosPagamentosStep_01":[[{"ultimosPagamentosReader":[{"xml_sql":["SELECT a.pgovlr, a.parnum, a.pgtdat, a.pcmdat, b.ramcod, b.aplcntnum, b.prporgcod, b.prpnum, c.angvctdat, c.nvavctdat, a.partotvlr FROM fgsmcmppar a LEFT JOIN fgsmcmpdct b ON a.cmpdctidecod = b.cmpdctidecod LEFT JOIN fgsmatrvctdct c ON b.aplcntnum = c.aplcntnum WHERE b.prporgcod IN ( 57, 67 ) AND b.ramcod IN ( 9531, 9746 ) AND a.atldat >= ? "]}]},{"ultimosPagamentosProcessor":[{"java_QUERY_BUSCA_PERCENTUAL_HONORARIO":["select hnrper from sramacd where acdcod = ? "]},{"java_QUERY_BUSCA_DATA_VENCIMENTO_VALOR_JUROS_PARCELA":["SELECT parvctdat, parjurvlr FROM sramacdpar WHERE acdcod = ? AND parnum = ? "]}]},{"ultimosPagamentosWriter":[{"xml_sqlContarParcelasVencidas":["SELECT COUNT(*) FROM sramacdpar WHERE acdcod = ? AND parnum > ? AND parsitcod = 3 "]},{"xml_sql":["UPDATE sramacdpar SET parpgtdat = ?, parvctdat = ?, parrcbvlr = ?, parsitcod = ?, parbxadat = ?, pgohnrvlr = ?, parjurvlr = ? WHERE acdcod = ? AND parnum = ?"]},{"env.email.service.url":["INSERT INTO sramprpmov (acdcod,acdsitcod,prpmovdat,ccajsttxt,altultdat,altultusrtipcod,altultusrempcod,altultusrmatnum) VALUES (?,?,?,?,?,?,?,?)"]}]}]]},{"acordosPagosStep_02":[[{"acordosPagosReader":[{"query.acordos.parcela.paga":["SELECT DISTINCT a.acdcod FROM sramacd a, sramacdpar p WHERE acdsitcod != 6 AND p.parsitcod = 1 AND a.acdcod = p.acdcod"]}]},{"acordosPagosProcessor":[{"java_QUERY_BUSCA_PARCELA_NAO_PAGA":["SELECT DISTINCT acdcod FROM sramacdpar WHERE acdcod = ? AND parsitcod != 1"]}]},{"acordosPagosCompositeWriter":[{"update.acordo.pago":["UPDATE sramacd SET acdsitcod = 6, altultdat = ? WHERE acdcod = ?"]},{"insert.movimento.acordo.pago":["INSERT INTO sramprpmov (acdcod, acdsitcod, prpmovdat, ccajsttxt, altultdat, altultusrtipcod, altultusrempcod, altultusrmatnum) VALUES (?, ?, ?, 'Acordo Pago', SYSDATE, 'P', 1, 6666)"]}]}]]},{"atualizacaoLoteFaturaPagaStep_03":[[{"atualizacaoLoteFaturaPagaReader":[{"query.ressarcimais.parcelas.pagas":["SELECT DISTINCT a.ftmlotnum, a.parbxadat FROM sramacdpar a, sramlotftmrcb b WHERE a.ftmlotnum = b.ftmlotnum AND b.ftmlotpgtdat IS NULL AND b.lotsttcod <> 4 AND a.ftmlotnum IS NOT NULL AND a.parsitcod = 1 "]}]},{"AtualizacaoLoteFaturaPagaProcessor":["loteFatura.setDataPagamento(parcela.getDataBaixa())","loteFatura.setCodigoStatusLote(SITUACAO_PAGA)","loteFatura.setDataUltimaAlteracao(new Date())","loteFatura.setCodigoEmpresaUsuarioUltimaAlteracao(01)","loteFatura.setCodigoTipoUsuarioUltimaAlteracao(F)","loteFatura.setNumeroMatriculaUsuarioUltimaAlteracao(6666)","loteFatura.setNumeroLote(parcela.getNumeroLoteFatura())"]},{"atualizacaoLoteFaturaPagaWriter":[{"update.ressarcimais.lote.fatura.paga":["UPDATE sramlotftmrcb SET ftmlotpgtdat = ?, lotsttcod = ?, altultdat = ?, altultusrempcod = ?, altultusrtipcod = ?, altultusrmatnum = ? WHERE ftmlotnum = ? "]}]}]]}]]}]

```
![image](src/assets/to_readme/TURBINA_EOLICA_V4.png)

  
 




