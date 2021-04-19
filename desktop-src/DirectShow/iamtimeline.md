---
description: L'interfaccia IAMTimeline fornisce metodi per la modifica della sequenza temporale, l'oggetto centrale in Microsoft DirectShow editing Services (DES).
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: Interfaccia IAMTimeline (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332049"
---
# <a name="iamtimeline-interface"></a>Interfaccia IAMTimeline

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMTimeline` interfaccia fornisce i metodi per modificare la sequenza temporale, ovvero l'oggetto centrale in Microsoft [DirectShow editing Services](directshow-editing-services.md) (des). Una sequenza temporale è una raccolta di elementi ordinati in tempo, ad esempio clip video, clip audio, effetti e transizioni tra clip. Il motore di rendering utilizza la sequenza temporale per creare un grafico di filtro, dal quale l'applicazione può generare l'output sottoposto a rendering.

`IAMTimeline` esegue tre servizi di base. Esso

-   Crea gli oggetti nella sequenza temporale.
-   Funge da contenitore per tali oggetti.
-   Imposta e recupera i parametri generali della sequenza temporale.

Per creare l'oggetto sequenza temporale, chiamare **CoCreateInstance** con l'identificatore di classe CLSID \_ AMTimeline.

## <a name="members"></a>Membri

L'interfaccia **IAMTimeline** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimeline** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimeline** dispone di questi metodi.



| Metodo                                                             | Descrizione                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**AddGroup**](iamtimeline-addgroup.md)                           | Aggiunge un gruppo alla sequenza temporale.<br/>                                                                                          |
| [**ClearAllGroups**](iamtimeline-clearallgroups.md)               | Rimuove tutti i gruppi dalla sequenza temporale, insieme a tutti gli oggetti contenuti in tali gruppi.<br/>                                |
| [**CreateEmptyNode**](iamtimeline-createemptynode.md)             | Crea un nuovo oggetto sequenza temporale.<br/>                                                                                         |
| [**EffectsEnabled**](iamtimeline-effectsenabled.md)               | Determina se gli effetti sono abilitati.<br/>                                                                                |
| [**EnableEffects**](iamtimeline-enableeffects.md)                 | Abilita o Disabilita tutti gli effetti nella sequenza temporale.<br/>                                                                       |
| [**EnableTransitions**](iamtimeline-enabletransitions.md)         | Abilita o Disabilita tutte le transizioni nella sequenza temporale.<br/>                                                                   |
| [**GetCountOfType**](iamtimeline-getcountoftype.md)               | Recupera il numero di oggetti del tipo specificato contenuti in un gruppo specificato e in tutti i relativi elementi figlio.<br/> |
| [**GetDefaultEffect**](iamtimeline-getdefaulteffect.md)           | Recupera l'effetto predefinito.<br/>                                                                                          |
| [**GetDefaultEffectB**](iamtimeline-getdefaulteffectb.md)         | Recupera l'effetto predefinito come valore **BSTR** .<br/>                                                                      |
| [**GetDefaultFPS**](iamtimeline-getdefaultfps.md)                 | Recupera la frequenza dei fotogrammi di output predefinita, in frame al secondo.<br/>                                                         |
| [**GetDefaultTransition**](iamtimeline-getdefaulttransition.md)   | Recupera la transizione predefinita.<br/>                                                                                      |
| [**GetDefaultTransitionB**](iamtimeline-getdefaulttransitionb.md) | Recupera la transizione predefinita come valore **BSTR** .<br/>                                                                  |
| [**GetDirtyRange**](iamtimeline-getdirtyrange.md)                 | Non supportata.<br/>                                                                                                         |
| [**GetDuration**](iamtimeline-getduration.md)                     | Recupera la durata della sequenza temporale.<br/>                                                                                       |
| [**GetDuration2**](iamtimeline-getduration2.md)                   | Recupera la durata della sequenza temporale come **valore Double**.<br/>                                                                       |
| [**GetGroup**](iamtimeline-getgroup.md)                           | Recupera un gruppo specificato.<br/>                                                                                           |
| [**GetGroupCount**](iamtimeline-getgroupcount.md)                 | Recupera il numero di gruppi contenuti nella sequenza temporale.<br/>                                                     |
| [**GetInsertMode**](iamtimeline-getinsertmode.md)                 | Non supportata.<br/>                                                                                                         |
| [**IsDirty**](iamtimeline-isdirty.md)                             | Non supportata.<br/>                                                                                                         |
| [**RemGroupFromList**](iamtimeline-remgroupfromlist.md)           | Non supportata.<br/>                                                                                                         |
| [**SetDefaultEffect**](iamtimeline-setdefaulteffect.md)           | Imposta l'effetto predefinito.<br/>                                                                                               |
| [**SetDefaultEffectB**](iamtimeline-setdefaulteffectb.md)         | Imposta l'effetto predefinito come valore **BSTR** .<br/>                                                                           |
| [**SetDefaultFPS**](iamtimeline-setdefaultfps.md)                 | Imposta la frequenza dei fotogrammi di output predefinita, in frame al secondo.<br/>                                                              |
| [**SetDefaultTransition**](iamtimeline-setdefaulttransition.md)   | Imposta la transizione predefinita.<br/>                                                                                           |
| [**SetDefaultTransitionB**](iamtimeline-setdefaulttransitionb.md) | Imposta la transizione predefinita come valore BSTR.<br/>                                                                           |
| [**SetInsertMode**](iamtimeline-setinsertmode.md)                 | Non implementato.<br/>                                                                                                       |
| [**SetInterestRange**](iamtimeline-setinterestrange.md)           | Non implementato.<br/>                                                                                                       |
| [**TransitionsEnabled**](iamtimeline-transitionsenabled.md)       | Determina se le transizioni sono abilitate.<br/>                                                                            |
| [**ValidateSourceNames**](iamtimeline-validatesourcenames.md)     | Convalida i nomi di origine nella sequenza temporale.<br/>                                                                                |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
