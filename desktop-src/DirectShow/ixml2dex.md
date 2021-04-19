---
description: L'interfaccia IXml2Dex Salva e carica i file di progetto di servizi di modifica DirectShow (DES) in Extensible Markup Language (XML). Questa interfaccia fornisce anche metodi per la lettura e la scrittura di file di grafico DirectShow (con estensione GRF).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Interfaccia IXml2Dex (qedit. h)
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
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332564"
---
# <a name="ixml2dex-interface"></a>Interfaccia IXml2Dex

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IXml2Dex` interfaccia Salva e carica i file di progetto di [servizi di modifica DirectShow](directshow-editing-services.md) (DES) in Extensible Markup Language (XML). Questa interfaccia fornisce anche metodi per la lettura e la scrittura di file di grafico DirectShow (con estensione GRF).

## <a name="members"></a>Membri

L'interfaccia **IXml2Dex** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IXml2Dex** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IXml2Dex** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**CopyXML**](ixml2dex-copyxml.md)                         | Non implementato.<br/>                                                |
| [**CreateGraphFromFile**](ixml2dex-creategraphfromfile.md) | Non implementato.<br/>                                                |
| [**Delete**](ixml2dex-delete.md)                           | Non implementato.<br/>                                                |
| [**PasteXML**](ixml2dex-pastexml.md)                       | Non implementato.<br/>                                                |
| [**PasteXMLFile**](ixml2dex-pastexmlfile.md)               | Non implementato.<br/>                                                |
| [**ReadXML**](ixml2dex-readxml.md)                         | Non implementato.<br/>                                                |
| [**ReadXMLFile**](ixml2dex-readxmlfile.md)                 | Carica un file di progetto XML.<br/>                                      |
| [**Reset**](ixml2dex-reset.md)                             | Non implementato.<br/>                                                |
| [**WriteGrfFile**](ixml2dex-writegrffile.md)               | Scrive un grafico di filtro in un file in formato. GRF.<br/>                 |
| [**WriteXML**](ixml2dex-writexml.md)                       | Converte una sequenza temporale in una stringa XML.<br/>                         |
| [**WriteXMLFile**](ixml2dex-writexmlfile.md)               | Converte una sequenza temporale in XML e scrive i dati XML in un file.<br/> |
| [**WriteXMLPart**](ixml2dex-writexmlpart.md)               | Non implementato.<br/>                                                |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Internet Explorer 4,0 o versione successiva<br/>                                               |
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
