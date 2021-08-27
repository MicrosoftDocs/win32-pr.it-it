---
title: Uso di macro per la gestione degli errori
description: COM definisce una serie di macro che semplificano l'uso dei valori HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f31280ec2076f8ece1fcf15dd6e27629a3016e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480537"
---
# <a name="using-macros-for-error-handling"></a>Uso di macro per la gestione degli errori

COM definisce una serie di macro che semplificano l'uso dei **valori HRESULT.**

Le macro di gestione degli errori sono descritte nella tabella seguente.




| Macro | Descrizione | 
|-------|-------------|
| <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br /> | Restituisce un <strong>HRESULT in</strong> base al bit di gravità, al codice della struttura e al codice di errore che costituiscono <strong>HRESULT.</strong><br /><blockquote>[!Note]<br />La <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> per S_OK verifica comporta una penalizzazione delle prestazioni. Non è consigliabile usare <strong>regolarmente</strong> MAKE_HRESULT per ottenere risultati positivi.</blockquote><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br /> | Restituisce uno <strong>SCODE in</strong> base al bit di gravità, al codice della struttura e al codice di errore che costituiscono <strong>SCODE.</strong><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br /> | Estrae la parte del codice di errore di <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br /> | Estrae il codice della struttura di <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br /> | Estrae il bit di gravità di <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br /> | Estrae la parte del codice di errore <strong>di SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br /> | Estrae il codice della struttura <strong>di SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br /> | Estrae il campo di gravità di <strong>SCODE.</strong><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>RIUSCITO</strong></a><br /> | Verifica il bit di gravità di <strong>SCODE</strong> o <strong>HRESULT;</strong> restituisce <strong>TRUE</strong> se la gravità è zero e <strong>FALSE</strong> se è uno.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FALLITO</strong></a><br /> | Verifica il bit di gravità di <strong>SCODE</strong> o <strong>HRESULT;</strong> restituisce <strong>TRUE</strong> se la gravità è pari a uno e <strong>FALSE</strong> se è zero.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br /> | Fornisce un test generico per gli errori in qualsiasi valore di stato. <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br /> | Mappe codice <a href="/windows/desktop/Debug/system-error-codes">di errore di sistema</a> in un <strong>valore HRESULT.</strong> <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br /> | Mappe un valore di stato NT in un <strong>valore HRESULT.</strong><br /> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](error-handling-in-com.md)
</dt> </dl>

 

