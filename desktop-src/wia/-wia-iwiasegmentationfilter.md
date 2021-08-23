---
description: L'interfaccia IWiaSegmentationFilter rileva le sottoaree di un flusso di immagini e crea elementi IWiaItem2 separati per ognuno.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Interfaccia IWiaSegmentationFilter (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 304b5be43aad8afc1730d2a23c170f11f11d319ffc4ae3eb13781efe09da2d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659701"
---
# <a name="iwiasegmentationfilter-interface"></a>Interfaccia IWiaSegmentationFilter

**L'interfaccia IWiaSegmentationFilter** rileva le sottoaree di un flusso di immagini e crea elementi [**IWiaItem2**](-wia-iwiaitem2.md) separati per ognuno.

## <a name="members"></a>Membri

**L'interfaccia IWiaSegmentationFilter** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaSegmentationFilter** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWiaSegmentationFilter** include questi metodi.



| Metodo                                                             | Descrizione                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) | Determina le sottoaree di un'immagine disposte sul pistoia piana in modo che ognuna delle sottoaree possa essere acquisita in un elemento immagine separato. <br/> |



 

## <a name="remarks"></a>Commenti

Un'applicazione deve [**usare IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) per creare una nuova istanza del filtro di segmentazione. Un'applicazione chiama in genere questa funzione prima di visualizzare la finestra di anteprima.

Quando si implementa questo filtro, usare [**IWiaItem2::CreateChildItem**](-wia-iwiaitem2-createchilditem.md) per creare gli elementi figlio. L'applicazione deve passare **COPY \_ PARENT PROPERTY \_ \_ VALUES** al parametro *ICreationFlags* per garantire che proprietà come il formato dell'immagine e la risoluzione siano uguali nell'elemento figlio appena creato come nell'elemento padre.

Un filtro di segmentazione deve supportare tutti i formati di immagine supportati dal driver con cui viene utilizzato. Il filtro fornito da Microsoft supporta bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) e Tagged Image File Format (TIFF).

Il filtro di segmentazione deve essere usato solo su elementi di film e scanner flat. Per l'analisi di film, uno scanner spesso viene fornito con fotogrammi fissi, nel qual caso il driver ha creato gli elementi figlio e l'applicazione non deve richiamare il filtro di segmentazione.

**L'interfaccia IWiaSegmentationFilter,** come tutte le Component Object Model (COM), eredita i metodi dell'interfaccia [IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Metodi IUnknown                                        | Descrizione                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Restituisce puntatori alle interfacce supportate. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa il conteggio dei riferimenti.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Riduce il conteggio dei riferimenti.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
