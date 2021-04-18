---
description: Gestisce i messaggi di errore e di stato del dispositivo durante i trasferimenti di dati di immagini e Visualizza i messaggi all'utente.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'Metodo IWiaAppErrorHandler:: ReportStatus (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308245"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a>Metodo IWiaAppErrorHandler:: ReportStatus

Gestisce i messaggi di errore e di stato del dispositivo durante i trasferimenti di dati di immagini e Visualizza i messaggi all'utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Non usato. Impostare su 0.

</dd> <dt>

*pWiaItem2* \[ in\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Puntatore all'elemento da trasferire.

</dd> <dt>

_hrStatus * \[ in\]
</dt> <dd>

Tipo: **HRESULT**

Codice di stato del dispositivo.

</dd> <dt>

*lPercentComplete* \[ in\]
</dt> <dd>

Tipo: **Long**

Percentuale di completamento dell'operazione corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Restituisce *hrStatus* se non è possibile recuperare l'errore. In caso contrario, restituisce uno dei valori seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | Se *hrStatus* è un errore, è stata eseguita l'azione appropriata per correggere l'errore e il trasferimento può continuare. Se *hrStatus* è informativo, l'utente è stato informato con una finestra di dialogo non modale e ha scelto di non annullare il trasferimento.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl>                  | L'utente ha annullato il trasferimento dalla finestra di dialogo non modale del gestore errori. Questo valore può essere restituito in qualsiasi momento, a prescindere dal tipo di *hrStatus* . <br/>                                                                                      |
| <dl> <dt>**\_stato WIA \_ non \_ gestito**</dt> </dl> | Non è stata eseguita alcuna azione. ovvero, nessuna finestra di dialogo è stata presentata all'utente. Verrà richiamato il gestore degli errori successivo. L'ordine dei gestori di errori è: applicazione, driver e impostazione predefinita del sistema.<br/>                                                 |



 

## <a name="remarks"></a>Commenti

Il parametro *lPercentComplete* consente a una finestra del gestore errori di visualizzare lo stato di avanzamento. Un driver, ad esempio, potrebbe fornire una stima del tempo necessario per il "riscaldamento". Il parametro *lPercentComplete* passato a **IWiaAppErrorHandler:: ReportStatus** è uguale al valore di **lPercentComplete** impostato dal driver nella struttura [**WiaTransferParams**](-wia-wiatransferparams.md) .

Un gestore degli errori può usare le macro SUCCEEDed e FAILED per verificare se *hrStatus* ha un errore di gravità o la gravità è riuscita \_ \_ .

Se *hrStatus* ha \_ esito positivo, l'utente deve essere autorizzato a annullare il trasferimento.

Se *hrStatus* è \_ un errore di gravità, il gestore degli errori dovrebbe visualizzare una finestra di dialogo modale di proprietà della finestra padre dell'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




