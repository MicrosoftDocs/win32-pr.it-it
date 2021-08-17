---
description: Gestisce lo stato del dispositivo e i messaggi di errore durante i trasferimenti di dati di immagine e visualizza i messaggi all'utente.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: Metodo IWiaAppErrorHandler::ReportStatus (Wia.h)
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
ms.openlocfilehash: 9cc727845489740fae54dcc96bf5bc903bceb0205688c1c60bee3df980f66845
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965750"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a>Metodo IWiaAppErrorHandler::ReportStatus

Gestisce lo stato del dispositivo e i messaggi di errore durante i trasferimenti di dati di immagine e visualizza i messaggi all'utente.

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

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Non usato. Impostare su 0.

</dd> <dt>

*pWiaItem2* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Puntatore all'elemento da trasferire.

</dd> <dt>

*hrStatus* \[ Pollici\]
</dt> <dd>

Tipo: **HRESULT**

Codice di stato del dispositivo.

</dd> <dt>

*lPercentComplete* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Percentuale completata dell'operazione corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Restituisce *hrStatus se* il recupero dall'errore non è possibile. In caso contrario, restituisce uno dei valori seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Se *hrStatus è* un errore, è stata eseguita l'azione appropriata per correggere l'errore e il trasferimento può continuare. Se *hrStatus è* informativo, l'utente è stato informato con una finestra di dialogo non modale e ha scelto di non annullare il trasferimento.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                  | L'utente ha annullato il trasferimento dalla finestra di dialogo non modabile del gestore degli errori. Questo valore può essere restituito in qualsiasi momento, indipendentemente da *hrStatus.* <br/>                                                                                      |
| <dl> <dt>**STATO WIA \_ \_ NON \_ GESTITO**</dt> </dl> | Non è stata eseguita alcuna azione. ciò significa che all'utente non è stata presentata alcuna finestra di dialogo. Verrà richiamato il gestore degli errori successivo. L'ordine dei gestori degli errori è: applicazione, driver e impostazione predefinita del sistema.<br/>                                                 |



 

## <a name="remarks"></a>Commenti

Il *parametro lPercentComplete* consente a una finestra del gestore errori di mostrare lo stato di avanzamento. Ad esempio, un driver potrebbe fornire una stima del tempo necessario per il "riscaldamento". Il *parametro lPercentComplete* passato in **IWiaAppErrorHandler::ReportStatus** corrisponde al valore di **lPercentComplete** impostato dal driver nella struttura [**WiaTransferParams.**](-wia-wiatransferparams.md)

Un gestore degli errori può usare le macro SUCCEEDED e FAILED per verificare se *hrStatus* ha SEVERITY \_ ERROR o SEVERITY \_ SUCCESS.

Se *hrStatus è* SEVERITY \_ SUCCESS, l'utente deve essere autorizzato ad annullare il trasferimento.

Se *hrStatus è* SEVERITY ERROR, il gestore degli errori dovrebbe visualizzare una finestra di dialogo \_ modale di proprietà della finestra padre dell'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




