---
description: Usato per impostare ed eseguire query sugli effetti e scegliere le tecniche. Un oggetto effetto può contenere più tecniche per eseguire il rendering dello stesso effetto.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: Interfaccia ID3DXEffect (D3DX9Effect.h)
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
ms.openlocfilehash: c9f5bdcf90b3e0d317290a569984d1b72d248079de5b3b281325e66af6e443c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494021"
---
# <a name="id3dxeffect-interface"></a>Interfaccia ID3DXEffect

Usato per impostare ed eseguire query sugli effetti e scegliere le tecniche. Un oggetto effetto può contenere più tecniche per eseguire il rendering dello stesso effetto.

## <a name="members"></a>Membri

**L'interfaccia ID3DXEffect** eredita da [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffect** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXEffect** include questi metodi.



| Metodo                                                                | Descrizione                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)       | Applicare i valori in un blocco di stato allo stato corrente del sistema degli effetti.<br/>                                                                                                                 |
| [**Inizia**](id3dxeffect--begin.md)                                   | Avvia una tecnica attiva.<br/>                                                                                                                                                           |
| [**BeginParameterBlock**](id3dxeffect--beginparameterblock.md)       | Avviare l'acquisizione delle modifiche dello stato in un blocco di parametri.<br/>                                                                                                                                   |
| [**BeginPass**](id3dxeffect--beginpass.md)                           | Avvia un passaggio, all'interno della tecnica attiva.<br/>                                                                                                                                           |
| [**CloneEffect**](id3dxeffect--cloneeffect.md)                       | Crea una copia di un effetto.<br/>                                                                                                                                                          |
| [**Commitchanges**](id3dxeffect--commitchanges.md)                   | Propagare le modifiche dello stato che si verificano all'interno di un passaggio attivo al dispositivo prima del rendering.<br/>                                                                                           |
| [**DeleteParameterBlock**](id3dxeffect--deleteparameterblock.md)     | Eliminare un blocco di parametri.<br/>                                                                                                                                                             |
| [**Fine**](id3dxeffect--end.md)                                       | Termina una tecnica attiva.<br/>                                                                                                                                                             |
| [**EndParameterBlock**](id3dxeffect--endparameterblock.md)           | Arrestare l'acquisizione delle modifiche dello stato dei parametri dell'effetto.<br/>                                                                                                                                        |
| [**EndPass**](id3dxeffect--endpass.md)                               | Terminare un passaggio attivo.<br/>                                                                                                                                                                   |
| [**FindNextValidTechnique**](id3dxeffect--findnextvalidtechnique.md) | Cerca la tecnica valida successiva, a partire dalla tecnica dopo la tecnica specificata.<br/>                                                                                       |
| [**GetCurrentTechnique**](id3dxeffect--getcurrenttechnique.md)       | Ottiene la tecnica corrente.<br/>                                                                                                                                                           |
| [**GetDevice**](id3dxeffect--getdevice.md)                           | Recupera il dispositivo associato all'effetto.<br/>                                                                                                                                      |
| [**GetPool**](id3dxeffect--getpool.md)                               | Ottiene un puntatore al pool di parametri condivisi.<br/>                                                                                                                                      |
| [**GetStateManager**](id3dxeffect--getstatemanager.md)               | Ottenere il gestore dello stato dell'effetto.<br/>                                                                                                                                                         |
| [**IsParameterUsed**](id3dxeffect--isparameterused.md)               | Determina se un parametro viene utilizzato dalla tecnica.<br/>                                                                                                                                   |
| [**OnLostDevice**](id3dxeffect--onlostdevice.md)                     | Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti i blocchi di stato. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.<br/> |
| [**OnResetDevice**](id3dxeffect--onresetdevice.md)                   | Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.<br/>                                                                                                                       |
| [**SetRawValue**](id3dxeffect--setrawvalue.md)                       | Impostare un intervallo contiguo di costanti shader con una copia della memoria.<br/>                                                                                                                        |
| [**SetStateManager**](id3dxeffect--setstatemanager.md)               | Impostare il gestore dello stato dell'effetto.<br/>                                                                                                                                                         |
| [**SetTechnique**](id3dxeffect--settechnique.md)                     | Imposta la tecnica attiva.<br/>                                                                                                                                                            |
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
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



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

 

 




