---
description: L'interfaccia IAMTimelineEffectable fornisce metodi per aggiungere effetti a un oggetto sequenza temporale in DirectShow Editing Services (DES) e per modificare gli effetti su un oggetto.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Interfaccia IAMTimelineEffectable (Qedit.h)
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
ms.openlocfilehash: ad6b373f4b30209566709117b3b15ecf1a65d093ddb2dd27e9e0273b11ad0b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905031"
---
# <a name="iamtimelineeffectable-interface"></a>Interfaccia IAMTimelineEffectable

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

L'interfaccia fornisce metodi per aggiungere effetti a un oggetto sequenza temporale in DirectShow Editing Services (DES) e per modificare gli `IAMTimelineEffectable` effetti su un oggetto. [](directshow-editing-services.md) Tutti gli oggetti a cui possono essere applicati effetti implementano questa interfaccia. sono incluse origini, tracce e composizioni.

Un oggetto che implementa questa interfaccia può avere un numero qualsiasi di effetti. Per ogni oggetto, il motore di rendering applica gli effetti in ordine di priorità, a partire dal livello di priorità 0.

## <a name="members"></a>Membri

**L'interfaccia IAMTimelineEffectable** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineEffectable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IAMTimelineEffectable.**



| Metodo                                                                     | Descrizione                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**EffectGetCount**](iamtimelineeffectable-effectgetcount.md)             | Recupera il numero di effetti sull'oggetto.<br/>                    |
| [**EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)           | Inserisce un effetto nell'oggetto al livello di priorità specificato.<br/> |
| [**EffectSwapPriorities**](iamtimelineeffectable-effectswappriorities.md) | Cambia i livelli di priorità di due effetti.<br/>                       |
| [**GetEffect**](iamtimelineeffectable-geteffect.md)                       | Recupera l'effetto al livello di priorità specificato.<br/>              |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
