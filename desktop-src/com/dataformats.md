---
title: DataFormats
description: Specifica i formati di dati predefiniti e principali supportati da un'applicazione.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- Chiave del registro di sistema DataFormats COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf130461a8db67cfe7fc7c56b0115b27eef6dc6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298907"
---
# <a name="dataformats"></a>DataFormats

Specifica i formati di dati predefiniti e principali supportati da un'applicazione.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a>Commenti

Il valore di *file/formato* specifica il file principale o il formato dell'oggetto predefinito per gli oggetti di questa classe.

Il valore *formats* specifica un elenco di formati per le implementazioni predefinite di [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), dove *n* è un indice Integer in base zero. Ad esempio, *n*  =  *Format*, *aspect*, *medium*, *flag*, dove *Format* è un formato degli Appunti, *aspect* è uno o più membri di [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *medium* è uno o più membri di [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)e *flag* è uno o più membri di [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IDataObject:: EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[**IDataObject:: SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




