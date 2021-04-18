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
# <a name="dataformats"></a><span data-ttu-id="f6a17-104">DataFormats</span><span class="sxs-lookup"><span data-stu-id="f6a17-104">DataFormats</span></span>

<span data-ttu-id="f6a17-105">Specifica i formati di dati predefiniti e principali supportati da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6a17-105">Specifies the default and main data formats supported by an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f6a17-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f6a17-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a><span data-ttu-id="f6a17-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6a17-107">Remarks</span></span>

<span data-ttu-id="f6a17-108">Il valore di *file/formato* specifica il file principale o il formato dell'oggetto predefinito per gli oggetti di questa classe.</span><span class="sxs-lookup"><span data-stu-id="f6a17-108">The *file/format* value specifies the default main file or object format for objects of this class.</span></span>

<span data-ttu-id="f6a17-109">Il valore *formats* specifica un elenco di formati per le implementazioni predefinite di [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), dove *n* è un indice Integer in base zero.</span><span class="sxs-lookup"><span data-stu-id="f6a17-109">The *formats* value specifies a list of formats for default implementations of [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), where *n* is a zero-based integer index.</span></span> <span data-ttu-id="f6a17-110">Ad esempio, *n*  =  *Format*, *aspect*, *medium*, *flag*, dove *Format* è un formato degli Appunti, *aspect* è uno o più membri di [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *medium* è uno o più membri di [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)e *flag* è uno o più membri di [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).</span><span class="sxs-lookup"><span data-stu-id="f6a17-110">For example, *n* = *format*, *aspect*, *medium*, *flag*, where *format* is a clipboard format, *aspect* is one or more members of [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *medium* is one or more members of [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed), and *flag* is one or more members of [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6a17-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6a17-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6a17-112">**IDataObject:: EnumFormatEtc**</span><span class="sxs-lookup"><span data-stu-id="f6a17-112">**IDataObject::EnumFormatEtc**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[<span data-ttu-id="f6a17-113">**IDataObject:: GetData**</span><span class="sxs-lookup"><span data-stu-id="f6a17-113">**IDataObject::GetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[<span data-ttu-id="f6a17-114">**IDataObject:: SetData**</span><span class="sxs-lookup"><span data-stu-id="f6a17-114">**IDataObject::SetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




