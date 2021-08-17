---
description: Questa sezione descrive un set di funzioni helper Windows usate con gli oggetti IPropertyBag.
ms.assetid: 4ef85855-7eb6-43ec-bf29-1223eaf1a0cc
title: Funzioni del contenitore delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b33bdcced7c030a476a3ec303ac30b5c5d0f722bceea5358678ba1a2fe6f790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970940"
---
# <a name="property-bag-functions"></a>Funzioni del contenitore delle proprietà

Questa sezione descrive un set di Windows helper usate con [**gli oggetti IPropertyBag.**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag)



| Argomento                                                                       | Contenuto                                                                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PSPropertyBag \_ Delete**](/windows/win32/api/propsys/nf-propsys-pspropertybag_delete)                     | Elimina una proprietà da un contenitore di proprietà.<br/>                                                                           |
| [**PSPropertyBag \_ ReadBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbool)                 | Legge il valore **dei dati BOOL** di una proprietà in un contenitore delle proprietà.<br/>                                                    |
| [**PSPropertyBag \_ ReadBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbstr)                 | Legge un valore **di dati BSTR** da una proprietà in un contenitore di proprietà.<br/>                                                    |
| [**PSPropertyBag \_ ReadDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readdword)               | Legge un valore **di dati DWORD** dalla proprietà in un contenitore delle proprietà.<br/>                                                     |
| [**PSPropertyBag \_ ReadGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readguid)                 | Legge il valore dei dati GUID da una proprietà in un contenitore di proprietà.<br/>                                                      |
| [**PSPropertyBag \_ ReadInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readint)                   | Legge un valore **di dati int** da una proprietà in un contenitore delle proprietà.<br/>                                                    |
| [**PSPropertyBag \_ ReadLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readlong)                 | Legge un valore **di dati LONG** da una proprietà in un contenitore di proprietà.<br/>                                                    |
| [**PSPropertyBag \_ ReadPOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpointl)             | Recupera le coordinate delle proprietà archiviate in una [**struttura POINTL**](/previous-versions//dd162807(v=vs.85)) di un contenitore di proprietà specificato.<br/>    |
| [**PSPropertyBag \_ ReadPOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpoints)             | Recupera le coordinate delle proprietà archiviate in una [**struttura POINTS**](/previous-versions//dd162808(v=vs.85)) di un contenitore di proprietà specificato.<br/>    |
| [**PSPropertyBag \_ ReadPropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpropertykey)   | Legge la chiave di proprietà di una proprietà in un contenitore di proprietà specificato.<br/>                                                 |
| [**PSPropertyBag \_ ReadRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readrectl)               | Recupera le coordinate di un rettangolo archiviato in una proprietà contenuta in un contenitore di proprietà specificato.<br/>              |
| [**PSPropertyBag \_ ReadSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readshort)               | Legge il valore **dei dati SHORT** di una proprietà in un contenitore delle proprietà.<br/>                                                   |
| [**PSPropertyBag \_ ReadStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstr)                   | Legge il valore **di dati** stringa di una proprietà in un contenitore delle proprietà.<br/>                                                  |
| [**PSPropertyBag \_ ReadStrAlloc**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstralloc)         | Legge un valore **di** dati stringa da una proprietà in un contenitore delle proprietà e alloca memoria per la stringa letta.<br/> |
| [**PSPropertyBag \_ ReadStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstream)             | Legge il flusso di dati archiviato in una determinata proprietà contenuta in un contenitore di proprietà specificato.<br/>                           |
| [**PSPropertyBag \_ ReadType**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readtype)                 | Legge il tipo di valore di dati di una proprietà archiviata in un contenitore delle proprietà.<br/>                                      |
| [**PSPropertyBag \_ ReadULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readulonglong)       | Legge un valore **di dati ULONGLONG** da una proprietà in un contenitore di proprietà.<br/>                                               |
| [**PSPropertyBag \_ ReadUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readunknown)           | Legge una determinata proprietà di un valore di dati sconosciuto in un contenitore di proprietà.<br/>                                                |
| [**PSPropertyBag \_ WriteBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebool)               | Imposta il **valore dei dati BOOL** di una proprietà in un contenitore delle proprietà.<br/>                                                     |
| [**PSPropertyBag \_ WriteBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebstr)               | Imposta un **valore di dati BSTR** da una proprietà in un contenitore di proprietà.<br/>                                                     |
| [**PSPropertyBag \_ WriteDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writedword)             | Imposta un **valore di dati DWORD** dalla proprietà in un contenitore delle proprietà.<br/>                                                      |
| [**PSPropertyBag \_ WriteGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeguid)               | Imposta il valore dei dati GUID da una proprietà in un contenitore delle proprietà.<br/>                                                       |
| [**PSPropertyBag \_ WriteInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeint)                 | Imposta un **valore di** dati int da una proprietà in un contenitore delle proprietà.<br/>                                                     |
| [**PSPropertyBag \_ WriteLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writelong)               | Imposta un **valore di** dati LONG da una proprietà in un contenitore di proprietà.<br/>                                                     |
| [**PSPropertyBag \_ WritePOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepointl)           | Archivia le coordinate delle proprietà archiviate in una [**struttura POINTL**](/previous-versions//dd162807(v=vs.85)) di un contenitore di proprietà specificato.<br/>       |
| [**PSPropertyBag \_ WritePOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepoints)           | Archivia le coordinate delle proprietà archiviate in una [**struttura POINTS**](/previous-versions//dd162808(v=vs.85)) di un contenitore di proprietà specificato.<br/>       |
| [**PSPropertyBag \_ WritePropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepropertykey) | Imposta la chiave di proprietà di una proprietà in un contenitore di proprietà specificato.<br/>                                                  |
| [**PSPropertyBag \_ WriteRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writerectl)             | Archivia le coordinate di un rettangolo archiviato in una proprietà contenuta in un contenitore di proprietà specificato.<br/>                 |
| [**PSPropertyBag \_ WriteSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeshort)             | Imposta il **valore dei** dati SHORT di una proprietà in un contenitore delle proprietà.<br/>                                                    |
| [**PSPropertyBag \_ WriteStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestr)                 | Imposta il **valore dei** dati stringa di una proprietà in un contenitore delle proprietà.<br/>                                                   |
| [**PSPropertyBag \_ WriteStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestream)           | Imposta il flusso di dati archiviato in una determinata proprietà contenuta in un contenitore di proprietà specificato.<br/>                            |
| [**PSPropertyBag \_ WriteULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeulonglong)     | Imposta un **valore di dati ULONGLONG** da una proprietà in un contenitore delle proprietà.<br/>                                                |
| [**PSPropertyBag \_ WriteUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeunknown)         | Imposta una determinata proprietà di un valore di dati sconosciuto in un contenitore di proprietà.<br/>                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni PROPVARIANT e VARIANT](./functions-propvarutil.md)
</dt> <dt>

[Funzioni](functions.md)
</dt> </dl>

 

 
