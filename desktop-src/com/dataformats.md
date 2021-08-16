---
title: Dataformats
description: Specifica i formati di dati predefiniti e principali supportati da un'applicazione.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- Chiave del Registro di sistema DATAFormats COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb8b2cc2ad4d11137fa41f419db2184f1a2b47fb850176227401e3d2b1aec04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310599"
---
# <a name="dataformats"></a>Dataformats

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

Il *valore file/formato* specifica il formato di oggetto o file principale predefinito per gli oggetti di questa classe.

Il *valore formats* specifica un elenco di formati per le implementazioni predefinite di [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), dove *n* è un indice integer in base zero. Ad esempio, *n* format , aspect , medium , flag , dove format è un formato degli Appunti, aspect è uno o più membri di  =     [**DVASPECT,**](/windows/win32/api/wtypes/ne-wtypes-dvaspect) *medium* è uno   o più membri di [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)e *flag* è uno o più membri di [**DATADIR.**](/windows/win32/api/objidl/ne-objidl-datadir)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[**IDataObject::SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




