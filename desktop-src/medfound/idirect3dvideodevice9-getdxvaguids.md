---
description: Ottiene un elenco di profili di accelerazione video DirectX (DXVA) supportati dal driver di visualizzazione.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'Metodo IDirect3DVideoDevice9:: GetDXVAGuids (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3ea05af8f27399af38419e177d7bd40b029cd63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310833"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a>Metodo IDirect3DVideoDevice9:: GetDXVAGuids

Ottiene un elenco di profili di accelerazione video DirectX (DXVA) supportati dal driver di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNumGuids* 
</dt> <dd>

In input, specifica il numero di elementi nella matrice *pGuids* . Se *pGuids* è **null**, il valore di `*pNumGuids` deve essere zero.

Nell'output, se *pGuids* è **null**, *pNumGuids* riceve il numero di profili DXVA in modalità limitata. In caso contrario, *pNumGuids* riceve il numero effettivo di GUID copiati nella matrice *pGuids* .

</dd> <dt>

*pGuids* 
</dt> <dd>

Indirizzo di una matrice di GUID o **null**. Se il valore è diverso da **null**, la matrice riceve un elenco di GUID che specificano i profili DXVA in modalità limitata. Questi GUID sono definiti in DXVA. h e sono documentati nella [specifica dxva 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Chiamare questo metodo due volte. Alla prima chiamata, impostare *pGuids* su **null**. Il parametro *pNumGuids* riceve il numero di GUID del profilo DXVA. Allocare una matrice di GUID con la dimensione richiesta e chiamare di nuovo il metodo. Questa volta, impostare *pGuids* sull'indirizzo della matrice. Il metodo riempie la matrice con l'elenco dei GUID del profilo DXVA.

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

 

 
