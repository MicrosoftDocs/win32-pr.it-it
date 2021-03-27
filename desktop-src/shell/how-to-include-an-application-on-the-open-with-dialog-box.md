---
description: Viene illustrato come verificare che l'applicazione venga visualizzata nel menu Apri con e nella finestra di dialogo per le applicazioni desktop ed è disponibile come app di Windows Store predefinita per i tipi di file specificati.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Come includere un'applicazione nella finestra di dialogo Apri con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881566"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a><span data-ttu-id="97163-103">Come includere un'applicazione nella finestra di dialogo Apri con</span><span class="sxs-lookup"><span data-stu-id="97163-103">How to Include an Application in the Open With Dialog Box</span></span>

<span data-ttu-id="97163-104">Viene illustrato come verificare che l'applicazione venga visualizzata nel menu **Apri con** e nella finestra di dialogo per le applicazioni desktop ed è disponibile come app di Windows Store predefinita per i tipi di file specificati.</span><span class="sxs-lookup"><span data-stu-id="97163-104">Illustrates how to ensure your application appears in the **Open With** menu and dialog box for desktop apps, and is available as a default Windows Store app for specified file types.</span></span>

## <a name="instructions"></a><span data-ttu-id="97163-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="97163-105">Instructions</span></span>

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a><span data-ttu-id="97163-106">Per ogni tipo di file, aggiungere l'applicazione alla sottochiave del registro di sistema OpenWithProgIds.</span><span class="sxs-lookup"><span data-stu-id="97163-106">For each file type, add your application to the OpenWithProgIds registry subkey.</span></span>

<span data-ttu-id="97163-107">Aggiungere il ProgID come nome di valore, con il tipo di valore REG \_ None o reg \_ SZ e una stringa vuota come valore di dati.</span><span class="sxs-lookup"><span data-stu-id="97163-107">Add your ProgID as a value name, with the value type of either REG\_NONE or REG\_SZ and an empty string as the data value.</span></span>

<span data-ttu-id="97163-108">Negli esempi di registro di sistema seguenti vengono illustrate le voci che associano InfoPath e per Microsoft Visual Studio con il tipo di file XML.</span><span class="sxs-lookup"><span data-stu-id="97163-108">The following registry examples show entries associating InfoPath and for Microsoft Visual Studio with the XML file type.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a><span data-ttu-id="97163-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="97163-109">Remarks</span></span>

<span data-ttu-id="97163-110">La sottochiave **OpenWithProgids** è preferibile a **OpenWithList** per identificare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97163-110">The **OpenWithProgids** subkey is preferred to **OpenWithList** to identify an application.</span></span> <span data-ttu-id="97163-111">Per ulteriori informazioni su queste sottochiavi, vedere [impostazione di sottochiavi facoltative e attributi di estensione del tipo di file](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="97163-111">For more information on these subkeys, see [Setting Optional Subkeys and File Type Extension Attributes](fa-file-types.md).</span></span>

<span data-ttu-id="97163-112">**OpenWithList** è destinato solo alle app legacy (solo con estensione exe) nei sistemi operativi precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="97163-112">**OpenWithList** is intended only for legacy apps (must be .exe only) on operating systems prior to Windows XP.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



