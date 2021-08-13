---
description: L'interfaccia IWiaPreview memorizza nella cache le immagini non filtrate internamente e le passa tramite i filtri di elaborazione delle immagini.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Interfaccia IWiaPreview (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e2672211e5c1a17fa360a6078069ae8260687dc896843ffb6bf572d9b7be8caa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442071"
---
# <a name="iwiapreview-interface"></a>Interfaccia IWiaPreview

**L'interfaccia IWiaPreview** memorizza nella cache le immagini non filtrate internamente e le passa tramite i filtri di elaborazione delle immagini.

## <a name="members"></a>Membri

**L'interfaccia IWiaPreview** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaPreview** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWiaPreview** include questi metodi.



| Metodo                                                  | Descrizione                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cancella**](-wia-iwiapreview-clear.md)                 | Rilascia l'immagine non filtrata memorizzata nella cache dal [**metodo IWiaPreview::GetNewPreview.**](-wia-iwiapreview-getnewpreview.md) Rilascia anche il filtro di elaborazione delle immagini. <br/>          |
| [**DetectRegions**](-wia-iwiapreview-detectregions.md) | Richiama il filtro di segmentazione del driver e passa l'immagine non filtrata memorizzata nella cache dal metodo [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) al filtro. <br/> |
| [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) | Memorizza nella cache internamente l'immagine non filtrata restituita dal driver. <br/>                                                                                                                |
| [**UpdatePreview**](-wia-iwiapreview-updatepreview.md) | Ottiene l'immagine non filtrata memorizzata nella cache dal [**metodo IWiaPreview::GetNewPreview.**](-wia-iwiapreview-getnewpreview.md) <br/>                                                            |



 

## <a name="remarks"></a>Commenti

Questo filtro viene chiamato automaticamente dal [**metodo IWiaTransfer::D ownload.**](-wia-iwiatransfer-download.md)

**L'interfaccia IWiaPreview,** come tutte le Component Object Model (COM), eredita i [metodi dell'interfaccia IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Metodi IUnknown                                        | Descrizione                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Restituisce puntatori alle interfacce supportate. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa il conteggio dei riferimenti.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Riduce il conteggio dei riferimenti.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
