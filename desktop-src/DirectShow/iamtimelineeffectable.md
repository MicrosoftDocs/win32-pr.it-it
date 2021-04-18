---
description: L'interfaccia IAMTimelineEffectable fornisce metodi per l'aggiunta di effetti a un oggetto Timeline nei servizi di modifica DirectShow (DES) e per la modifica degli effetti su un oggetto.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Interfaccia IAMTimelineEffectable (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328155"
---
# <a name="iamtimelineeffectable-interface"></a>Interfaccia IAMTimelineEffectable

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMTimelineEffectable` interfaccia fornisce metodi per l'aggiunta di effetti a un oggetto Timeline in [servizi di modifica DirectShow](directshow-editing-services.md) (des) e per la modifica degli effetti su un oggetto. Tutti gli oggetti che possono avere effetti applicati implementano questa interfaccia; sono incluse origini, tracce e composizioni.

Un oggetto che implementa questa interfaccia può avere un numero qualsiasi di effetti. Per ogni oggetto, il motore di rendering applica gli effetti in ordine di priorità, a partire dal livello di priorità 0.

## <a name="members"></a>Membri

L'interfaccia **IAMTimelineEffectable** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineEffectable** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimelineEffectable** dispone di questi metodi.



| Metodo                                                                     | Descrizione                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**EffectGetCount**](iamtimelineeffectable-effectgetcount.md)             | Recupera il numero di effetti su questo oggetto.<br/>                    |
| [**EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)           | Inserisce un effetto nell'oggetto al livello di priorità specificato.<br/> |
| [**EffectSwapPriorities**](iamtimelineeffectable-effectswappriorities.md) | Passa i livelli di priorità di due effetti.<br/>                       |
| [**GetEffect**](iamtimelineeffectable-geteffect.md)                       | Recupera l'effetto al livello di priorità specificato.<br/>              |



 

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



 

 
