---
description: Eseguire il commit di tutte le modifiche apportate a una mesh al dispositivo, in modo che sia possibile eseguire il rendering delle modifiche. Questa operazione deve essere chiamata dopo che i dati di una mesh vengono modificati e prima che ne venga eseguito il rendering. Non è possibile eseguire il rendering di una mesh a meno che non ne venga eseguito il commit nel dispositivo. Vedere la sezione Osservazioni.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'Metodo ID3DX10Mesh:: CommitToDevice (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058616"
---
# <a name="id3dx10meshcommittodevice-method"></a>Metodo ID3DX10Mesh:: CommitToDevice

Eseguire il commit di tutte le modifiche apportate a una mesh al dispositivo, in modo che sia possibile eseguire il rendering delle modifiche. Questa operazione deve essere chiamata dopo che i dati di una mesh vengono modificati e prima che ne venga eseguito il rendering. Non è possibile eseguire il rendering di una mesh a meno che non ne venga eseguito il commit nel dispositivo. Vedere la sezione Osservazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Quando viene caricata una mesh, i dati vengono caricati nelle risorse di staging, ovvero i dati possono essere modificati ma non sottoposti a rendering. Quando viene chiamato CommitToDevice, i dati delle risorse di gestione temporanea vengono copiati nelle risorse del dispositivo in modo che possano essere sottoposti a rendering. Sebbene i dati vengano sottoposte a commit nel dispositivo, le risorse di gestione temporanea rimangono e possono essere modificate. Se vengono apportate modifiche alle risorse di gestione temporanea, è necessario eseguire di nuovo il commit delle risorse di gestione temporanea sul dispositivo per poter eseguire il rendering delle modifiche sullo schermo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




