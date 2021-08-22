---
description: Eseguire il commit delle modifiche apportate a una mesh nel dispositivo in modo che sia possibile eseguire il rendering delle modifiche. Questa operazione deve essere chiamata dopo che i dati di una mesh sono stati modificati e prima che ne venga eseguito il rendering. Non è possibile eseguire il rendering di una mesh a meno che non ne venga eseguito il commit nel dispositivo. Vedere la sezione Osservazioni.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: Metodo ID3DX10Mesh::CommitToDevice (D3DX10.h)
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
ms.openlocfilehash: 50dde79e57ca7edf838f05b1fa1b4d10f5da5cc936b3cbf563c7838703650806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567031"
---
# <a name="id3dx10meshcommittodevice-method"></a>Metodo ID3DX10Mesh::CommitToDevice

Eseguire il commit delle modifiche apportate a una mesh nel dispositivo in modo che sia possibile eseguire il rendering delle modifiche. Questa operazione deve essere chiamata dopo che i dati di una mesh sono stati modificati e prima che ne venga eseguito il rendering. Non è possibile eseguire il rendering di una mesh a meno che non ne venga eseguito il commit nel dispositivo. Vedere la sezione Osservazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Quando una mesh viene caricata, i dati vengono caricati nelle risorse di staging, vale a dire che i dati possono essere modificati ma non sottoposti a rendering. Quando viene chiamato CommitToDevice, i dati delle risorse di staging vengono copiati nelle risorse del dispositivo in modo da poter essere sottoposti a rendering. Anche se viene eseguito il commit dei dati nel dispositivo, le risorse di staging rimangono e possono essere modificate. Se vengono apportate modifiche alle risorse di staging, è necessario eseguire nuovamente il commit delle risorse di staging nel dispositivo per poterne eseguire il rendering sullo schermo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




