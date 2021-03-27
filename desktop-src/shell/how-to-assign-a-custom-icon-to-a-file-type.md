---
description: Un'icona personalizzata deve essere assegnata a un tipo di file per fornire un'indicazione visiva all'utente di quel tipo di file o all'applicazione a cui è associato il tipo di file.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Come assegnare un'icona personalizzata a un tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979618"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a><span data-ttu-id="ebf09-103">Come assegnare un'icona personalizzata a un tipo di file</span><span class="sxs-lookup"><span data-stu-id="ebf09-103">How to Assign a Custom Icon to a File Type</span></span>

<span data-ttu-id="ebf09-104">Quando nessuna icona personalizzata predefinita viene assegnata a un tipo di file, il desktop e Windows Explorer visualizzano tutti i file di quel tipo con un'icona generica predefinita.</span><span class="sxs-lookup"><span data-stu-id="ebf09-104">When no custom default icon is assigned to a file type, the desktop and Windows Explorer display all files of that type with a generic default icon.</span></span> <span data-ttu-id="ebf09-105">Ad esempio, lo screenshot seguente Mostra questa icona predefinita usata con il file MyDocs4. MYP.</span><span class="sxs-lookup"><span data-stu-id="ebf09-105">For example, the following screen shot shows this default icon used with the MyDocs4.myp file.</span></span>

![screenshot dell'icona predefinita](images/icon.png)

<span data-ttu-id="ebf09-107">Mentre tutti i file visualizzati in questa schermata sono semplici file di testo, solo MyDocs4. MYP Visualizza l'icona predefinita di Windows.</span><span class="sxs-lookup"><span data-stu-id="ebf09-107">While all the files displayed in this screen shot are simple text files, only MyDocs4.myp displays the Windows default icon.</span></span> <span data-ttu-id="ebf09-108">Questo è dovuto al fatto che l'estensione txt è un tipo di file registrato con un'icona predefinita personalizzata.</span><span class="sxs-lookup"><span data-stu-id="ebf09-108">This is because the .txt extension is a registered file type that has a custom default icon.</span></span>

<span data-ttu-id="ebf09-109">Lo screenshot seguente mostra un'icona personalizzata che è stata assegnata al tipo di file. MYP.</span><span class="sxs-lookup"><span data-stu-id="ebf09-109">The following screen shot shows a custom icon that has been assigned to the .myp file type.</span></span>

![screenshot dell'icona personalizzata per i file con estensione MYP](images/context4.png)

> [!Note]  
> <span data-ttu-id="ebf09-111">Le icone possono essere assegnate anche in base a un'applicazione specifica.</span><span class="sxs-lookup"><span data-stu-id="ebf09-111">Icons can also be assigned on an application-specific basis.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="ebf09-112">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="ebf09-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="ebf09-113">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="ebf09-113">Step 1:</span></span>

<span data-ttu-id="ebf09-114">Creare una sottochiave denominata **DefaultIcon** in una delle due posizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ebf09-114">Create a subkey named **DefaultIcon** in one of the following two locations:</span></span>

-   <span data-ttu-id="ebf09-115">Per un'assegnazione del tipo di file, **HKEY \_ classi \_ radice** \\ *. Extension*</span><span class="sxs-lookup"><span data-stu-id="ebf09-115">For a file-type assignment, **HKEY\_CLASSES\_ROOT**\\ *.extension*</span></span>
-   <span data-ttu-id="ebf09-116">Per l'assegnazione di un'applicazione, **HKEY \_ classi \_ radice** \\ *ProgID*</span><span class="sxs-lookup"><span data-stu-id="ebf09-116">For an application assignment, **HKEY\_CLASSES\_ROOT**\\*ProgID*</span></span>

### <a name="step-2"></a><span data-ttu-id="ebf09-117">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="ebf09-117">Step 2:</span></span>

<span data-ttu-id="ebf09-118">Assegnare la sottochiave **DefaultIcon** un valore predefinito di tipo **reg \_ SZ** che specifica il percorso completo del file che contiene l'icona.</span><span class="sxs-lookup"><span data-stu-id="ebf09-118">Assign the **DefaultIcon** subkey a default value of type **REG\_SZ** that specifies the fully qualified path for the file that contains the icon.</span></span>

### <a name="step-3"></a><span data-ttu-id="ebf09-119">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="ebf09-119">Step 3:</span></span>

<span data-ttu-id="ebf09-120">Chiamare la funzione [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) per notificare alla shell di aggiornare la cache delle icone.</span><span class="sxs-lookup"><span data-stu-id="ebf09-120">Call the [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) function to notify the Shell to update its icon cache.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf09-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebf09-121">Remarks</span></span>

<span data-ttu-id="ebf09-122">Nell'esempio seguente viene illustrata una visualizzazione dettagliata delle voci del registro di sistema necessarie per l'assegnazione di un'icona di tipo file.</span><span class="sxs-lookup"><span data-stu-id="ebf09-122">The following example shows a detailed view of the registry entries that are required for a file-type icon assignment.</span></span> <span data-ttu-id="ebf09-123">L'estensione del nome file è associata a un'applicazione, ma l'assegnazione dell'icona è all'estensione del nome file, in modo che l'applicazione associata non stabilisca l'icona predefinita.</span><span class="sxs-lookup"><span data-stu-id="ebf09-123">The file name extension is associated with an application, but the icon assignment is to the file name extension itself so that the associated application does not dictate the default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="ebf09-124">Nell'esempio seguente viene illustrata una visualizzazione dettagliata delle voci del registro di sistema necessarie per l'assegnazione di un'icona dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ebf09-124">The following example shows a detailed view of the registry entries that are required for an application icon assignment.</span></span> <span data-ttu-id="ebf09-125">L'estensione del nome di file. MYP viene prima associata all'applicazione Program. 1.</span><span class="sxs-lookup"><span data-stu-id="ebf09-125">The .myp file name extension is first associated with the MyProgram.1 application.</span></span> <span data-ttu-id="ebf09-126">Alla sottochiave ProgID Program. 1 viene quindi assegnata l'icona predefinita personalizzata.</span><span class="sxs-lookup"><span data-stu-id="ebf09-126">The MyProgram.1 ProgID subkey is then assigned the custom default icon.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

<span data-ttu-id="ebf09-127">Tutti i file che contengono un'icona sono accettabili, inclusi i file ICO, exe e dll.</span><span class="sxs-lookup"><span data-stu-id="ebf09-127">Any file that contains an icon is acceptable, including .ico, .exe, and .dll files.</span></span> <span data-ttu-id="ebf09-128">Se nel file è presente più di un'icona, il percorso deve essere seguito da una virgola e quindi dall'indice dell'icona.</span><span class="sxs-lookup"><span data-stu-id="ebf09-128">If there is more than one icon in the file, the path should be followed by a comma, and then the index of the icon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebf09-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ebf09-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebf09-130">Tipi di file</span><span class="sxs-lookup"><span data-stu-id="ebf09-130">File Types</span></span>](fa-file-types.md)
</dt> </dl>

 

 



