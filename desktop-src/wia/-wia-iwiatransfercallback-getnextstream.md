---
description: Ottiene un nuovo flusso per l'elemento specificato.
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'Metodo IWiaTransferCallback:: GetNextStream (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307353"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a>Metodo IWiaTransferCallback:: GetNextStream

Ottiene un nuovo flusso per l'elemento specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Attualmente non usato. Deve essere impostato su zero.

</dd> <dt>

*bstrItemName* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome dell'elemento per cui creare il flusso.

</dd> <dt>

*bstrFullItemName* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome completo dell'elemento per il quale creare il flusso.

</dd> <dt>

*ppDestination* \[ out\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***

Riceve l'indirizzo di un puntatore al nuovo oggetto [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Quando questo metodo viene implementato da un filtro di elaborazione delle immagini, Windows Image Acquisition (WIA) 2,0 minidriver lo chiama durante l'acquisizione dell'immagine per ottenere il flusso di destinazione dal client.

Un filtro **IWiaTransferCallback:: GetNextStream** deve delegare al metodo di callback dell'applicazione. Il filtro usa il flusso restituito dall'implementazione **IWiaTransferCallback:: GetNextStream** del callback dell'applicazione per creare il proprio flusso che passa di nuovo al servizio WIA 2,0. Il filtro viene eseguito quando il flusso del filtro chiama il metodo [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) .

Il flusso del filtro non può ipotizzare il numero di byte scritti in ogni scrittura, poiché i dati dell'immagine non filtrata possono provenire dal componente WIA 2,0 Preview anziché dal driver. Il componente WIA 2,0 Preview scrive sempre tutti i dati dell'immagine non filtrati nel flusso del filtro una sola volta, il che significa che il flusso del filtro contiene una scrittura di origine. Se il driver e il componente di anteprima vengono scritti nel flusso del filtro, il flusso del filtro non può presumere, ad esempio, che riceva l'intestazione completa la prima volta che [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) viene chiamato, sebbene il driver corrispondente scriva sempre i dati dell'intestazione prima in un'unica operazione di scrittura. Non è possibile presupporre che una scrittura successiva contenga esattamente una riga di analisi. Il flusso di filtro potrebbe quindi dover contare il numero di byte scritti per determinare, ad esempio, dove vengono avviati i dati dell'immagine.

L'implementazione di **IWiaTransferCallback:: GetNextStream** del filtro di elaborazione delle immagini deve leggere le proprietà necessarie per l'elaborazione delle immagini dall'elemento per il quale viene acquisita l'immagine. Il filtro non legge le proprietà direttamente da *pWiaItem2* passato in [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md). Il filtro deve invece chiamare [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) su questo elemento WIA 2,0 per ottenere l'elemento WIA 2,0 effettivo. Il motivo è che l'immagine acquisita può effettivamente essere un elemento figlio di *pWiaItem2*. Ad esempio, durante l'acquisizione di una cartella il filtro usa *pWiaItem2* per ottenere gli elementi figlio di *pWiaItem2* in **IWiaTransferCallback:: GetNextStream** (durante l'acquisizione di una cartella, il driver restituisce le immagini rappresentate dagli elementi figlio di *pWiaItem2*). Lo stesso accade quando il componente WIA 2,0 Preview chiama il filtro di elaborazione dell'immagine passando un elemento WIA 2,0 figlio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
