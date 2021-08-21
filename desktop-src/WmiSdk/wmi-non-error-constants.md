---
description: Codici restituiti WMI che indicano lo stato e non indicano un errore.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Costanti wmi non di errore (WbemCli.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651013d89577e1f8c336dd1b070cdb0c8476fe73206c681371c0ad84bfa99fa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107022"
---
# <a name="wmi-non-error-constants"></a>Costanti wmi non di errore

Codici restituiti WMI che indicano lo stato e non indicano un errore.

Se un'operazione non restituisce un errore, WMI restituisce uno dei codici seguenti come **HRESULT** che indica lo stato dell'operazione.

> [!Note]  
> Alcuni metodi nelle classi WMI possono restituire codici di errore di sistema e di rete (ad esempio 64). È possibile controllare la definizione di questi tipi di codici di errore usando il **comando net helpmsg** nella finestra del prompt dei comandi. Ad esempio, il comando **net helpmsg 64** restituisce il messaggio: Il nome di rete specificato non è più disponibile.

 

In C++ è possibile chiamare [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e specificare **C: \\ Windows \\ System32 \\ wbem \\wmiutils.dll** come modulo del messaggio.

<dl> <dt>

<span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM \_ S \_ NO \_ ERROR**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



L'operazione è stata completata.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ FALSE**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Non sono disponibili altri oggetti, il numero di oggetti restituiti è minore del numero richiesto o si tratta della fine di un'enumerazione. Questo valore viene restituito anche quando questo metodo viene chiamato con valore 0 per il *parametro uCount.*


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S \_ ESISTE \_ GIÀ**
</dt> <dd> <dl> <dt>

262145 (0x40001)
</dt> <dt>



È stato effettuato un tentativo di creare un oggetto o una classe già esistente.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM \_ S \_ \_ REIMPOSTATO SUL VALORE \_ PREDEFINITO**
</dt> <dd> <dl> <dt>

262146 (0x40002)
</dt> <dt>



Una proprietà sottoposta a override è stata eliminata. Questo valore viene restituito per segnalare che il valore originale non sottoposto a override è stato ripristinato in seguito all'eliminazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ DIVERSO**
</dt> <dd> <dl> <dt>

262147 (0x40003)
</dt> <dt>



Gli elementi (oggetti, classi e così via) che vengono confrontati non sono identici.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**TIMEDOUT DI WBEM \_ S \_**
</dt> <dd> <dl> <dt>

262148 (0x40004)
</dt> <dt>



Timeout di una chiamata. Non si tratta di una condizione di errore. Pertanto, è possibile che siano stati restituiti anche alcuni risultati.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ S NON PIÙ \_ \_ \_ DATI**
</dt> <dd> <dl> <dt>

262149 (0x40005)
</dt> <dt>



Non sono disponibili altri dati dall'enumerazione e l'utente deve terminare l'enumerazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**OPERAZIONE \_ WBEM S \_ \_ ANNULLATA**
</dt> <dd> <dl> <dt>

262150 (0x40006)
</dt> <dt>



L'operazione è stata annullata intenzionalmente o inavvicinatamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ IN SOSPESO**
</dt> <dd> <dl> <dt>

262151 (0x40007)
</dt> <dt>



Una richiesta è ancora in corso e i risultati non sono ancora disponibili.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**OGGETTI DUPLICATI \_ WBEM S \_ \_**
</dt> <dd> <dl> <dt>

262152 (0x40008)
</dt> <dt>



Sono state individuate più copie dello stesso oggetto nel gruppo di risultati di un'enumerazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**ACCESSO WBEM \_ S \_ \_ NEGATO**
</dt> <dd> <dl> <dt>

262153 (0x40009)
</dt> <dt>



All'utente è stato negato l'accesso ad alcune risorse, ma non a tutte.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**RISULTATI PARZIALI DI WBEM \_ S \_ \_**
</dt> <dd> <dl> <dt>

262160 (0x40010)
</dt> <dt>



L'utente non ha ricevuto tutti gli oggetti richiesti a causa di risorse inaccessibili (diverse da violazioni della sicurezza).


</dt> </dl> </dd> <dt>

<span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**SERVIZIO LIMITATO \_ WBEM S \_ \_**
</dt> <dd> <dl> <dt>

274433 (0x43001)
</dt> <dt>



Il provider è in grado di eseguire un servizio limitato.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM \_ S \_ AGGIORNATO INDIRETTAMENTE \_**
</dt> <dd> <dl> <dt>

274434 (0x43002)
</dt> <dt>



Riservato per utilizzi futuri.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>WbemCli.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WbemCli.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici restituiti WMI](wmi-return-codes.md)
</dt> </dl>

 

