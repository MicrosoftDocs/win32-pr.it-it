---
description: Ottiene un elenco di formati pixel non compressi di cui è possibile eseguire il rendering utilizzando un profilo di accelerazione video DirectX (DXVA) specificato.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'Metodo IDirect3DVideoDevice9:: GetUncompressedDXVAFormats (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345076"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a>Metodo IDirect3DVideoDevice9:: GetUncompressedDXVAFormats

Ottiene un elenco di formati pixel non compressi di cui è possibile eseguire il rendering utilizzando un profilo di accelerazione video DirectX (DXVA) specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGuid* 
</dt> <dd>

Puntatore a un GUID che specifica il profilo DXVA. Per ottenere un elenco dei profili supportati, chiamare [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pNumFormats* 
</dt> <dd>

In input, specifica il numero di elementi nella matrice *pFormats* . Se *pFormats* è **null**, il valore di `*pNumFormats` deve essere zero.

Nell'output, se *pFormats* è **null**, *pNumFormats* riceve il numero di formati di pixel supportati. In caso contrario, *pNumFormats* riceve il numero effettivo di formati pixel copiati nella matrice *pFormats* .

</dd> <dt>

*pFormats* 
</dt> <dd>

Indirizzo di una matrice di valori **D3DFORMAT** o **null**. Se il valore è diverso da **null**, la matrice riceve un elenco di formati pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Chiamare questo metodo due volte. Alla prima chiamata, impostare *pFormats* su **null**. Il parametro *pNumFormats* riceve il numero di formati. Allocare una matrice **D3DFORMAT** con le dimensioni richieste e chiamare di nuovo il metodo. Questa volta, impostare *pFormats* sull'indirizzo della matrice. Il metodo riempie la matrice con l'elenco dei formati pixel.

Il driver deve restituire i formati in ordine di preferenza decrescente, con il formato preferito elencato per primo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




