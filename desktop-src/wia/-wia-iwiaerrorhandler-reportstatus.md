---
description: Gestisce i messaggi di stato e di errore durante il trasferimento dei dati dell'immagine e li visualizza all'utente.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'Metodo IWiaErrorHandler:: ReportStatus (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312399"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a>Metodo IWiaErrorHandler:: ReportStatus

Gestisce i messaggi di stato e di errore durante il trasferimento dei dati dell'immagine e li visualizza all'utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Tipo: **HWND**

**HWND** che rappresenta la finestra padre della finestra di messaggio.

</dd> <dt>

*punkItem* \[ in\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Puntatore all'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'elemento da trasferire. Questo oggetto implementa almeno [_ *IWiaItem2* *](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ in\]
</dt> <dd>

Tipo: **HRESULT**

**HRESULT** che rappresenta il codice di stato ricevuto da [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*cbResLength* \[ in\]
</dt> <dd>

Tipo: **Long**

**Long** che corrisponde alla dimensione dei dati a cui fa riferimento *pbData*.

</dd> <dt>

*pbData* \[ in\]
</dt> <dd>

Tipo: **byte \** _

Puntatore al buffer di dati ricevuto da [_ *BandedDataCallback* *](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Restituisce *hrStatus* se l'errore non può essere recuperato da. In caso contrario, restituisce uno dei valori seguenti.



| Codice restituito                                                                             | Descrizione                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | È stata eseguita l'azione appropriata per correggere l'errore e il trasferimento può continuare. <br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | Non è stata eseguita alcuna azione per gestire lo stato dell'errore o del report all'utente. <br/>                |
| <dl> <dt>**\_Interrompi E**</dt> </dl> | L'utente ha scelto di interrompere il trasferimento in risposta alla finestra di dialogo visualizzata. <br/>        |



 

## <a name="remarks"></a>Commenti

Windows Image Acquisition (WIA) 2,0 chiama **IWiaErrorHandler:: ReportStatus** quando il driver invia un messaggio di **\_ \_ \_ stato del dispositivo msg it** a [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback). Questo metodo gestisce il messaggio e visualizza all'utente le informazioni sullo stato o sull'errore. Se il messaggio riguarda un errore, il metodo consente all'utente di scegliere, se possibile, se provare a correggere l'errore e continuare il trasferimento o interrompere.

*hrStatus* è impostato su WIA \_ stato \_ trasferimento \_ inizio per informare il gestore che è stato avviato un trasferimento. Viene impostato su WIA \_ status \_ Transfer end al termine \_ del trasferimento.

Se *hrStatus* ha \_ esito positivo, l'utente deve essere autorizzato a annullare il trasferimento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
