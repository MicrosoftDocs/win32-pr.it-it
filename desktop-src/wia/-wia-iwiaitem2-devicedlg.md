---
description: Visualizza una finestra di dialogo per preparare l'acquisizione dell'immagine.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: Metodo IWiaItem2::D eviceDlg (Wia.h)
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
ms.openlocfilehash: c9eaab17f0a76bfc5c6ac919a9abef92ca7288539c9705ca30c02b1dd0a8d1ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118035222"
---
# <a name="iwiaitem2devicedlg-method"></a>Metodo IWiaItem2::D eviceDlg

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

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Specifica un set di flag che controllano l'operazione della finestra di dialogo. Il valore può essere 0 per rappresentare il comportamento predefinito o uno dei flag WIA DEVICE DIALOG descritti \_ \_ in [**WiaFlag**](-wia-wiaflag.md).

</dd> <dt>

*hwndParent* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Handle per la finestra padre.

</dd> <dt>

*bstrFolderName* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome della cartella in cui devono essere trasferiti i file.

</dd> <dt>

*bstrFilename* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome del file modello.

</dd> <dt>

*plNumFiles* \[ Pollici\]
</dt> <dd>

Tipo: **\* LONG**

Puntatore al numero di elementi nella matrice *ppbstrFilePaths.*

</dd> <dt>

*ppbstrFilePaths* \[ in, out\]
</dt> <dd>

Tipo: **BSTR \* \***

Indirizzo di un puntatore a una matrice di percorsi per i file analizzati. Inizializzare il puntatore in modo che punti a una matrice di dimensioni zero (0) prima che venga chiamato **IWiaItem2::D eviceDlg.**

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Indirizzo di una matrice di puntatori alle [**interfacce IWiaItem2.**](-wia-iwiaitem2.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo visualizza una finestra di dialogo per l'utente che un'applicazione usa per raccogliere tutte le informazioni necessarie per l'acquisizione dell'immagine. Viene inoltre usato per specificare le proprietà di analisi dell'immagine, ad esempio luminosità e contrasto.

Al termine di questo metodo, l'applicazione può usare [**l'interfaccia IWiaTransfer**](-wia-iwiatransfer.md) per acquisire l'immagine.

Le applicazioni devono chiamare il [metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per ogni elemento nella matrice di puntatori a interfaccia ricevuti tramite il *parametro ppIWiaItem2.* Le applicazioni devono anche liberare la matrice [usando CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
