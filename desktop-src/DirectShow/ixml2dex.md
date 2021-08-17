---
description: L'interfaccia IXml2Dex salva e carica DirectShow di progetto DES (Editing Services) in Extensible Markup Language (XML). Questa interfaccia fornisce anche metodi per la lettura e la scrittura DirectShow file di grafo (con estensione grf).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Interfaccia IXml2Dex (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3bc12c2305a8b92110d4aa17522184e9a3c5ee83b60ccd5a989468fa0a8c6e7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952390"
---
# <a name="ixml2dex-interface"></a>Interfaccia IXml2Dex

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`IXml2Dex`L'interfaccia salva e carica DirectShow di progetto DES [(Editing Services)](directshow-editing-services.md) in Extensible Markup Language (XML). Questa interfaccia fornisce anche metodi per la lettura e la scrittura DirectShow file di grafo (con estensione grf).

## <a name="members"></a>Membri

**L'interfaccia IXml2Dex** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IXml2Dex** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IXml2Dex** include questi metodi.



| Metodo                                                      | Descrizione                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**CopyXML**](ixml2dex-copyxml.md)                         | Non implementato.<br/>                                                |
| [**CreateGraphFromFile**](ixml2dex-creategraphfromfile.md) | Non implementato.<br/>                                                |
| [**Elimina**](ixml2dex-delete.md)                           | Non implementato.<br/>                                                |
| [**PasteXML**](ixml2dex-pastexml.md)                       | Non implementato.<br/>                                                |
| [**PasteXMLFile**](ixml2dex-pastexmlfile.md)               | Non implementato.<br/>                                                |
| [**Readxml**](ixml2dex-readxml.md)                         | Non implementato.<br/>                                                |
| [**ReadXMLFile**](ixml2dex-readxmlfile.md)                 | Carica un file di progetto XML.<br/>                                      |
| [**Reset**](ixml2dex-reset.md)                             | Non implementato.<br/>                                                |
| [**WriteGrfFile**](ixml2dex-writegrffile.md)               | Scrive un grafo di filtro in un file in formato grf.<br/>                 |
| [**WriteXML**](ixml2dex-writexml.md)                       | Converte una sequenza temporale in una stringa XML.<br/>                         |
| [**WriteXMLFile**](ixml2dex-writexmlfile.md)               | Converte una sequenza temporale in XML e scrive i dati XML in un file.<br/> |
| [**WriteXMLPart**](ixml2dex-writexmlpart.md)               | Non implementato.<br/>                                                |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Internet Explorer 4.0 o versione successiva<br/>                                               |
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
