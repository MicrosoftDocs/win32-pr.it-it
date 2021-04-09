---
description: Visualizza una finestra di dialogo per preparare l'acquisizione dell'immagine.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: Metodo IWiaItem2::D eviceDlg (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129430"
---
# <a name="iwiaitem2devicedlg-method"></a>IWiaItem2::D Metodo eviceDlg

Visualizza una finestra di dialogo per preparare l'acquisizione dell'immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica un set di flag che controllano l'operazione della finestra di dialogo. Il valore può essere 0 per rappresentare il comportamento predefinito o uno dei \_ flag della finestra di dialogo del dispositivo WIA \_ descritti in [**WiaFlag**](-wia-wiaflag.md).

</dd> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Tipo: **HWND**

Handle per la finestra padre.

</dd> <dt>

*bstrFolderName* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome della cartella in cui devono essere trasferiti i file.

</dd> <dt>

*bstrFilename* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome del file modello.

</dd> <dt>

*plNumFiles* \[ in\]
</dt> <dd>

Tipo: **Long \** _

Puntatore al numero di elementi nella matrice _ppbstrFilePaths *.

</dd> <dt>

*ppbstrFilePaths* \[ in uscita\]
</dt> <dd>

Tipo: **BSTR \* \***

Indirizzo di un puntatore a una matrice di percorsi per i file analizzati. Inizializzare il puntatore in modo che punti a una matrice di dimensioni zero (0) prima di **IWiaItem2::D evicedlg** viene chiamato.

</dd> <dt>

*ppIWiaItem2* \[ in uscita\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Indirizzo di una matrice di puntatori alle interfacce [**IWiaItem2**](-wia-iwiaitem2.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo Visualizza una finestra di dialogo per l'utente che viene utilizzata da un'applicazione per raccogliere tutte le informazioni necessarie per l'acquisizione delle immagini. Viene anche usato per specificare le proprietà di analisi dell'immagine, ad esempio luminosità e contrasto.

Dopo la restituzione di questo metodo, l'applicazione può utilizzare l'interfaccia [**IWiaTransfer**](-wia-iwiatransfer.md) per acquisire l'immagine.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per ogni elemento nella matrice di puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* . Le applicazioni devono inoltre liberare la matrice utilizzando [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
