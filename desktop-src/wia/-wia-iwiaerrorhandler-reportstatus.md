---
description: Gestisce i messaggi di stato e di errore durante i trasferimenti di dati di immagine e li visualizza all'utente.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: Metodo IWiaErrorHandler::ReportStatus (Wia.h)
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
ms.openlocfilehash: 6604dc8dbf0cad5f31449ff3cc30945c1e6059727d513fa98dbf436eb199f70f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659751"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a>Metodo IWiaErrorHandler::ReportStatus

Gestisce i messaggi di stato e di errore durante i trasferimenti di dati di immagine e li visualizza all'utente.

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

*hwndParent* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

**HWND** che rappresenta la finestra padre per la finestra di messaggio.

</dd> <dt>

*itemItem* \[ Pollici\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntatore [all'interfaccia IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'elemento da trasferire. Questo oggetto implementa in modo minimo [**IWiaItem2**](-wia-iwiaitem2.md) e [**IWiaDataTransfer.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)

</dd> <dt>

*hrStatus* \[ Pollici\]
</dt> <dd>

Tipo: **HRESULT**

**HRESULT** che è il codice di stato ricevuto da [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> <dt>

*cbResLength* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

**LONG** che rappresenta le dimensioni dei dati a cui fa riferimento *pbData*.

</dd> <dt>

*pbData* \[ Pollici\]
</dt> <dd>

Tipo: **\* BYTE**

Puntatore al buffer di dati ricevuto da [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Restituisce *hrStatus* se non è possibile recuperare l'errore. In caso contrario, restituisce uno dei valori seguenti.



| Codice restituito                                                                             | Descrizione                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | È stata eseguita l'azione appropriata per correggere l'errore e il trasferimento può continuare. <br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Non è stata eseguita alcuna azione per gestire l'errore o segnalare lo stato all'utente. <br/>                |
| <dl> <dt>**E \_ ABORT**</dt> </dl> | L'utente ha scelto di interrompere il trasferimento in risposta alla finestra di dialogo visualizzata. <br/>        |



 

## <a name="remarks"></a>Commenti

Windows Acquisizione di immagini (WIA) 2.0 chiama **IWiaErrorHandler::ReportStatus** quando il driver invia un messaggio DI STATO DEL DISPOSITIVO **\_ MSG \_ \_ IT** a [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback) Questo metodo gestisce il messaggio e visualizza all'utente informazioni sullo stato o sull'errore. Se il messaggio riguarda un errore, il metodo consente all'utente di scegliere, se possibile, se tentare di eseguire il ripristino dall'errore e continuare il trasferimento o interrompere l'operazione.

*hrStatus è* impostato su WIA \_ STATUS TRANSFER BEGIN per \_ \_ informare il gestore che è stato avviato un trasferimento. È impostato su WIA \_ STATUS TRANSFER END al termine del \_ \_ trasferimento.

Se *hrStatus è* SEVERITY \_ SUCCESS, l'utente deve essere autorizzato ad annullare il trasferimento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
