---
description: Codici restituiti WMI che indicano lo stato e non indicano un errore.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Costanti non di errore WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226939"
---
# <a name="wmi-non-error-constants"></a>Costanti non di errore WMI

Codici restituiti WMI che indicano lo stato e non indicano un errore.

Se un'operazione non genera un errore, WMI restituisce uno dei seguenti codici come **HRESULT** che indica lo stato dell'operazione.

> [!Note]  
> Alcuni metodi delle classi WMI possono restituire codici di errore di sistema e di rete (ad esempio, 64). È possibile controllare la definizione di questi tipi di codici di errore usando il comando **net helpmsg** nella finestra del prompt dei comandi. Ad esempio, il comando **net helpmsg 64** restituisce il messaggio: il nome di rete specificato non è più disponibile.

 

In C++ è possibile chiamare [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e specificare **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** come modulo Message.

<dl> <dt>

<span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**\_non è \_ disponibile alcun \_ errore in WBEM**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



L'operazione è stata completata.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ false**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Non sono disponibili altri oggetti, il numero di oggetti restituiti è inferiore al numero richiesto oppure è la fine di un'enumerazione. Questo valore viene restituito anche quando questo metodo viene chiamato con un valore pari a 0 per il parametro *uCount* .


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S \_ \_ esiste già**
</dt> <dd> <dl> <dt>

262145 (0x40001)
</dt> <dt>



È stato effettuato un tentativo di creare un oggetto o una classe già esistente.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**il \_ ripristino di WBEM S è \_ \_ \_ predefinito**
</dt> <dd> <dl> <dt>

262146 (0x40002)
</dt> <dt>



Una proprietà sottoposta a override è stata eliminata. Questo valore viene restituito per segnalare che il valore originale non sottoposto a override è stato ripristinato in seguito all'eliminazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ diverso**
</dt> <dd> <dl> <dt>

262147 (0x40003)
</dt> <dt>



Gli elementi (oggetti, classi e così via) che vengono confrontati non sono identici.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**timeout di WBEM \_ S \_**
</dt> <dd> <dl> <dt>

262148 (0x40004)
</dt> <dt>



Si è verificato il timeout di una chiamata. Non si tratta di una condizione di errore. È pertanto possibile che vengano restituiti anche alcuni risultati.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**\_ \_ non sono disponibili \_ altri \_ dati per WBEM**
</dt> <dd> <dl> <dt>

262149 (0x40005)
</dt> <dt>



Non sono disponibili altri dati dall'enumerazione e l'utente deve terminare l'enumerazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**\_operazione WBEM \_ \_ annullata**
</dt> <dd> <dl> <dt>

262150 (0x40006)
</dt> <dt>



L'operazione è stata annullata intenzionalmente o involontariamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ in sospeso**
</dt> <dd> <dl> <dt>

262151 (0x40007)
</dt> <dt>



Una richiesta è ancora in corso e i risultati non sono ancora disponibili.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**\_ \_ oggetti duplicati WBEM S \_**
</dt> <dd> <dl> <dt>

262152 (0x40008)
</dt> <dt>



Sono state individuate più copie dello stesso oggetto nel gruppo di risultati di un'enumerazione.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**accesso a WBEM \_ S \_ \_ negato**
</dt> <dd> <dl> <dt>

262153 (0x40009)
</dt> <dt>



All'utente è stato negato l'accesso ad alcune risorse, ma non a tutte.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_ \_ risultati parziali di WBEM \_**
</dt> <dd> <dl> <dt>

262160 (0x40010)
</dt> <dt>



L'utente non ha ricevuto tutti gli oggetti richiesti a causa di risorse inaccessibili (ad eccezione delle violazioni della sicurezza).


</dt> </dl> </dd> <dt>

<span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**servizio con limitazioni per WBEM \_ S \_ \_**
</dt> <dd> <dl> <dt>

274433 (0x43001)
</dt> <dt>



Il provider è in grado di limitare il servizio.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM \_ è \_ stato \_ aggiornato indirettamente**
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
| Intestazione<br/>                   | <dl> <dt>WbemCli. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WbemCli. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici restituiti WMI](wmi-return-codes.md)
</dt> </dl>

 

