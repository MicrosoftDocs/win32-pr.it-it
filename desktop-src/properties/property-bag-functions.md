---
description: In questa sezione viene descritto un set di funzioni di supporto di Windows utilizzate con gli oggetti IPropertyBag.
ms.assetid: 4ef85855-7eb6-43ec-bf29-1223eaf1a0cc
title: Funzioni contenitore delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c86a2e3ce61805702641f893d51f5c4aa26b0ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313532"
---
# <a name="property-bag-functions"></a>Funzioni contenitore delle proprietà

In questa sezione viene descritto un set di funzioni di supporto di Windows utilizzate con gli oggetti [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) .



| Argomento                                                                       | Contenuto                                                                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Eliminazione di PSPropertyBag \_**](/windows/win32/api/propsys/nf-propsys-pspropertybag_delete)                     | Elimina una proprietà da un contenitore di proprietà.<br/>                                                                           |
| [**\_ReadBOOL PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbool)                 | Legge il valore di dati **bool** di una proprietà in un contenitore delle proprietà.<br/>                                                    |
| [**\_ReadBSTR PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbstr)                 | Legge un valore di dati **BSTR** da una proprietà in un contenitore delle proprietà.<br/>                                                    |
| [**\_ReadDWORD PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readdword)               | Legge un valore di dati **DWORD** dalla proprietà in un contenitore di proprietà.<br/>                                                     |
| [**\_ReadGUID PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readguid)                 | Legge il valore dei dati GUID da una proprietà in un contenitore delle proprietà.<br/>                                                      |
| [**\_ReadInt PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readint)                   | Legge un valore di dati **int** da una proprietà in un contenitore delle proprietà.<br/>                                                    |
| [**\_ReadLONG PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readlong)                 | Legge un valore di dati **Long** da una proprietà in un contenitore delle proprietà.<br/>                                                    |
| [**\_ReadPOINTL PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpointl)             | Recupera le coordinate della proprietà archiviate in una struttura [**POINTL**](/previous-versions//dd162807(v=vs.85)) di un contenitore di proprietà specificato.<br/>    |
| [**\_ReadPOINTS PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpoints)             | Recupera le coordinate della proprietà archiviate in una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) di un contenitore di proprietà specificato.<br/>    |
| [**\_ReadPropertyKey PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpropertykey)   | Legge la chiave della proprietà di una proprietà in un contenitore di proprietà specificato.<br/>                                                 |
| [**\_ReadRECTL PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readrectl)               | Recupera le coordinate di un rettangolo archiviato in una proprietà contenuta in un contenitore di proprietà specificato.<br/>              |
| [**\_ReadSHORT PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readshort)               | Legge il valore dei dati **brevi** di una proprietà in un contenitore delle proprietà.<br/>                                                   |
| [**\_ReadStr PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstr)                   | Legge il valore dei dati **stringa** di una proprietà in un contenitore delle proprietà.<br/>                                                  |
| [**\_ReadStrAlloc PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstralloc)         | Legge un valore di dati **stringa** da una proprietà in un elenco di proprietà e alloca memoria per la stringa che viene letta.<br/> |
| [**\_ReadStream PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstream)             | Legge il flusso di dati archiviato in una determinata proprietà contenuta in un contenitore di proprietà specificato.<br/>                           |
| [**\_ReadType PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readtype)                 | Legge il tipo di valore dei dati di una proprietà archiviata in un contenitore delle proprietà.<br/>                                      |
| [**\_ReadULONGLONG PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readulonglong)       | Legge un valore di dati **ULONGLONG** da una proprietà in un contenitore delle proprietà.<br/>                                               |
| [**\_ReadUnknown PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readunknown)           | Legge una determinata proprietà di un valore di dati sconosciuto in un contenitore delle proprietà.<br/>                                                |
| [**\_WriteBOOL PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebool)               | Imposta il valore di dati **bool** di una proprietà in un contenitore delle proprietà.<br/>                                                     |
| [**\_WriteBSTR PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebstr)               | Imposta un valore di dati **BSTR** da una proprietà in un contenitore delle proprietà.<br/>                                                     |
| [**\_WriteDWORD PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writedword)             | Imposta un valore di dati **DWORD** dalla proprietà in un contenitore delle proprietà.<br/>                                                      |
| [**\_WriteGUID PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeguid)               | Imposta il valore dei dati GUID da una proprietà in un contenitore delle proprietà.<br/>                                                       |
| [**\_WriteInt PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeint)                 | Imposta un valore di dati **int** da una proprietà in un contenitore delle proprietà.<br/>                                                     |
| [**\_WriteLONG PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writelong)               | Imposta un valore di dati **Long** da una proprietà in un contenitore delle proprietà.<br/>                                                     |
| [**\_WritePOINTL PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepointl)           | Archivia le coordinate della proprietà archiviate in una struttura [**POINTL**](/previous-versions//dd162807(v=vs.85)) di un contenitore di proprietà specificato.<br/>       |
| [**\_WritePOINTS PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepoints)           | Archivia le coordinate della proprietà archiviate in una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) di un contenitore di proprietà specificato.<br/>       |
| [**\_WritePropertyKey PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepropertykey) | Imposta la chiave della proprietà di una proprietà in un contenitore di proprietà specificato.<br/>                                                  |
| [**\_WriteRECTL PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writerectl)             | Archivia le coordinate di un rettangolo archiviato in una proprietà contenuta in un contenitore di proprietà specificato.<br/>                 |
| [**\_WriteSHORT PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeshort)             | Imposta il valore dei dati **brevi** di una proprietà in un contenitore delle proprietà.<br/>                                                    |
| [**\_WriteStr PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestr)                 | Imposta il valore dei dati **stringa** di una proprietà in un contenitore delle proprietà.<br/>                                                   |
| [**\_WriteStream PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestream)           | Imposta il flusso di dati archiviato in una determinata proprietà contenuta in un contenitore di proprietà specificato.<br/>                            |
| [**\_WriteULONGLONG PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeulonglong)     | Imposta un valore di dati **ULONGLONG** da una proprietà in un contenitore delle proprietà.<br/>                                                |
| [**\_WriteUnknown PSPropertyBag**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeunknown)         | Imposta una proprietà specificata di un valore di dati sconosciuto in un contenitore delle proprietà.<br/>                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni PROPVARIANT e VARIANT](./functions-propvarutil.md)
</dt> <dt>

[Funzioni](functions.md)
</dt> </dl>

 

 
