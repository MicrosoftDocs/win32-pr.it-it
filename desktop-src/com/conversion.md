---
title: Conversione
description: Utilizzato dalla finestra di dialogo Converti per determinare i formati che possono essere letti e scritti da un'applicazione.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Conversione della chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516072"
---
# <a name="conversion"></a><span data-ttu-id="b4cdc-104">Conversione</span><span class="sxs-lookup"><span data-stu-id="b4cdc-104">Conversion</span></span>

<span data-ttu-id="b4cdc-105">Utilizzato dalla finestra di dialogo **Converti** per determinare i formati che possono essere letti e scritti da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b4cdc-105">Used by the **Convert** dialog box to determine the formats an application can read and write.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b4cdc-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b4cdc-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a><span data-ttu-id="b4cdc-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4cdc-107">Remarks</span></span>

<span data-ttu-id="b4cdc-108">Le informazioni sulla conversione vengono utilizzate dalla finestra di dialogo **Converti** per determinare i formati che possono essere letti e scritti da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b4cdc-108">Conversion information is used by the **Convert** dialog box to determine what formats an application can read and write.</span></span> <span data-ttu-id="b4cdc-109">Un formato di file delimitato da virgole è indicato da un numero se è uno dei formati degli Appunti definiti in Windows. h.</span><span class="sxs-lookup"><span data-stu-id="b4cdc-109">A comma-delimited file format is indicated by a number if it is one of the Clipboard formats defined in Windows.h.</span></span> <span data-ttu-id="b4cdc-110">Una stringa indica che il formato non è definito in Windows. h (privato).</span><span class="sxs-lookup"><span data-stu-id="b4cdc-110">A string indicates the format is not one defined in Windows.h (private).</span></span> <span data-ttu-id="b4cdc-111">In questo caso, il formato leggibile e scrivibile è la \_ struttura CF (privata).</span><span class="sxs-lookup"><span data-stu-id="b4cdc-111">In this case, the readable and writable format is CF\_OUTLINE (private).</span></span>

<span data-ttu-id="b4cdc-112">Il valore *rformat* specifica il formato di file che un'applicazione può leggere (da cui eseguire la conversione).</span><span class="sxs-lookup"><span data-stu-id="b4cdc-112">The *rformat* value specifies the file format an application can read (convert from).</span></span>

<span data-ttu-id="b4cdc-113">Il valore *rwformat* specifica il formato di file che un'applicazione può leggere e scrivere (attivare come).</span><span class="sxs-lookup"><span data-stu-id="b4cdc-113">The *rwformat* value specifies the file format an application can read and write (activate as).</span></span>

 

 




