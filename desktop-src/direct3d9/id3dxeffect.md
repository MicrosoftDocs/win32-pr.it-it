---
description: Utilizzato per impostare ed eseguire query sugli effetti e per scegliere tecniche. Un oggetto Effect può contenere più tecniche per il rendering dello stesso effetto.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: Interfaccia ID3DXEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275376234739964940d70381a34331ff5b89f2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322350"
---
# <a name="id3dxeffect-interface"></a>Interfaccia ID3DXEffect

Utilizzato per impostare ed eseguire query sugli effetti e per scegliere tecniche. Un oggetto Effect può contenere più tecniche per il rendering dello stesso effetto.

## <a name="members"></a>Membri

L'interfaccia **ID3DXEffect** eredita da [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffect** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXEffect** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)       | Applicare i valori in un blocco di stato allo stato del sistema con effetto corrente.<br/>                                                                                                                 |
| [**Inizia**](id3dxeffect--begin.md)                                   | Avvia una tecnica attiva.<br/>                                                                                                                                                           |
| [**BeginParameterBlock**](id3dxeffect--beginparameterblock.md)       | Avviare l'acquisizione delle modifiche di stato in un blocco di parametri.<br/>                                                                                                                                   |
| [**BeginPass**](id3dxeffect--beginpass.md)                           | Inizia un passaggio, all'interno della tecnica attiva.<br/>                                                                                                                                           |
| [**CloneEffect**](id3dxeffect--cloneeffect.md)                       | Crea una copia di un effetto.<br/>                                                                                                                                                          |
| [**CommitChanges**](id3dxeffect--commitchanges.md)                   | Propagare le modifiche di stato che si verificano all'interno di un passaggio attivo al dispositivo prima del rendering.<br/>                                                                                           |
| [**DeleteParameterBlock**](id3dxeffect--deleteparameterblock.md)     | Elimina un blocco di parametri.<br/>                                                                                                                                                             |
| [**Fine**](id3dxeffect--end.md)                                       | Termina una tecnica attiva.<br/>                                                                                                                                                             |
| [**EndParameterBlock**](id3dxeffect--endparameterblock.md)           | Arresta l'acquisizione delle modifiche allo stato del parametro dell'effetto.<br/>                                                                                                                                        |
| [**EndPass**](id3dxeffect--endpass.md)                               | Termina un passaggio attivo.<br/>                                                                                                                                                                   |
| [**FindNextValidTechnique**](id3dxeffect--findnextvalidtechnique.md) | Cerca la tecnica valida successiva, iniziando dalla tecnica dopo la tecnica specificata.<br/>                                                                                       |
| [**GetCurrentTechnique**](id3dxeffect--getcurrenttechnique.md)       | Ottiene la tecnica corrente.<br/>                                                                                                                                                           |
| [**GetDevice**](id3dxeffect--getdevice.md)                           | Recupera il dispositivo associato all'effetto.<br/>                                                                                                                                      |
| [**GetPool**](id3dxeffect--getpool.md)                               | Ottiene un puntatore al pool di parametri condivisi.<br/>                                                                                                                                      |
| [**GetStateManager**](id3dxeffect--getstatemanager.md)               | Ottenere il gestore degli Stati dell'effetto.<br/>                                                                                                                                                         |
| [**IsParameterUsed**](id3dxeffect--isparameterused.md)               | Determina se un parametro viene utilizzato dalla tecnica.<br/>                                                                                                                                   |
| [**OnLostDevice**](id3dxeffect--onlostdevice.md)                     | Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.<br/> |
| [**OnResetDevice**](id3dxeffect--onresetdevice.md)                   | Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.<br/>                                                                                                                       |
| [**SetRawValue**](id3dxeffect--setrawvalue.md)                       | Impostare un intervallo contiguo di costanti dello shader con una copia di memoria.<br/>                                                                                                                        |
| [**SetStateManager**](id3dxeffect--setstatemanager.md)               | Impostare il gestore degli Stati dell'effetto.<br/>                                                                                                                                                         |
| [**Setechnique**](id3dxeffect--settechnique.md)                     | Imposta la tecnica attiva.<br/>                                                                                                                                                            |
| [**ValidateTechnique**](id3dxeffect--validatetechnique.md)           | Convalidare una tecnica.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

L'interfaccia ID3DXEffect viene ottenuta chiamando [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)o [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).

Il tipo LPD3DXEFFECT è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Interfacce degli effetti](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> <dt>

[**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




