---
description: L'interfaccia IWiaSegmentationFilter rileva le aree secondarie di un flusso di immagini e crea elementi IWiaItem2 separati per ognuno di essi.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Interfaccia IWiaSegmentationFilter (WIA. h)
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
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879318"
---
# <a name="iwiasegmentationfilter-interface"></a>Interfaccia IWiaSegmentationFilter

L'interfaccia **IWiaSegmentationFilter** rileva le aree secondarie di un flusso di immagini e crea elementi [**IWiaItem2**](-wia-iwiaitem2.md) separati per ognuno di essi.

## <a name="members"></a>Membri

L'interfaccia **IWiaSegmentationFilter** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaSegmentationFilter** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWiaSegmentationFilter** dispone di questi metodi.



| Metodo                                                             | Descrizione                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) | Determina le aree secondarie di un'immagine disposte sulla piastra piana, in modo che ogni area secondaria possa essere acquisita in un elemento immagine separato. <br/> |



 

## <a name="remarks"></a>Commenti

Un'applicazione deve usare [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) per creare una nuova istanza del filtro di segmentazione. Un'applicazione in genere chiama questa funzione prima di visualizzarne la finestra di anteprima.

Quando si implementa questo filtro, utilizzare [**IWiaItem2:: CreateChildItem**](-wia-iwiaitem2-createchilditem.md) per creare gli elementi figlio. L'applicazione deve passare **i \_ \_ \_ valori della proprietà copia padre** al parametro *ICreationFlags* per garantire che le proprietà, ad esempio il formato di immagine e la risoluzione, siano le stesse nell'elemento figlio appena creato come nell'elemento padre.

Un filtro di segmentazione deve supportare tutti i formati di immagine supportati dal driver. Il filtro fornito da Microsoft supporta bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) e Tagged Image File Format (TIFF).

Il filtro di segmentazione deve essere utilizzato solo su elementi di film e scanner di piano. Per l'analisi dei film, uno scanner spesso è dotato di frame fissi, nel qual caso il driver ha creato gli elementi figlio e l'applicazione non deve richiamare il filtro di segmentazione.

L'interfaccia **IWiaSegmentationFilter** , come tutte le interfacce Component Object Model (com), eredita i metodi di interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Metodi IUnknown                                        | Descrizione                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Restituisce puntatori alle interfacce supportate. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa il conteggio dei riferimenti.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Riduce il conteggio dei riferimenti.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
