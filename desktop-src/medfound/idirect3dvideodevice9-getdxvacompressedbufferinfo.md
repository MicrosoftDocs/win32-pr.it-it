---
description: Ottiene informazioni sui buffer compressi necessari per la decodifica con accelerazione hardware.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: Metodo IDirect3DVideoDevice9::GetDXVACompressedBufferInfo (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: efb96ec457cdb81f89982947bf1b9bc40543789b2e9ac253d83c81727f1efae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942291"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a>Metodo IDirect3DVideoDevice9::GetDXVACompressedBufferInfo

Ottiene informazioni sui buffer compressi necessari per la decodifica con accelerazione hardware.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGuid* 
</dt> <dd>

Puntatore a un GUID che specifica il profilo DXVA. Per ottenere un elenco dei profili supportati, chiamare [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pUncompData* 
</dt> <dd>

Puntatore a [**una struttura DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) che specifica le dimensioni e il formato pixel dei dati non compressi.

</dd> <dt>

*pNumBuffers* 
</dt> <dd>

Nell'input specifica il numero di elementi nella *matrice pBufferInfo.* Se *pBufferInfo* è **NULL,** il valore di `*pNumBuffers` deve essere zero.

Nell'output, se *pBufferInfo* è **NULL,** *pNumBuffers* riceve le dimensioni della matrice da allocare. In caso *contrario, pNumBuffers* riceve il numero effettivo di elementi copiati nella *matrice pBufferInfo.*

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Indirizzo di una matrice [**di strutture DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) o **NULL.** Se il valore è diverso **da NULL,** il metodo copia un elenco **di strutture DXVACompBufferInfo** in questa matrice. Ogni struttura corrisponde a un tipo di buffer di dati compressi usato dall'acceleratore video.

Impostare tutti gli elementi della matrice su zero prima di chiamare questo metodo.

Ogni indice di matrice corrisponde a uno dei tipi di superficie DXVA definiti in dxva.h. L'acceleratore video restituisce un elenco di voci fino a **DXVA \_ NUM TYPES COMP \_ \_ \_ BUFFERS** array. Per informazioni dettagliate, vedere la [specifica DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration), sezione 3.4, "Buffer Description List". Se un particolare tipo di buffer non viene utilizzato dal profilo DXVA, la voce in corrispondenza di tale indice contiene zeri per tutti i valori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                    |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 
