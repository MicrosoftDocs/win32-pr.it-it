---
description: Definizione degli attributi dei tipi di file nel registro di sistema.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Come definire gli attributi del tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7844c65191d6513a06625a28c47accd3df5cc82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881574"
---
# <a name="how-to-define-file-type-attributes"></a><span data-ttu-id="c685d-103">Come definire gli attributi del tipo di file</span><span class="sxs-lookup"><span data-stu-id="c685d-103">How to Define File Type Attributes</span></span>

<span data-ttu-id="c685d-104">L'assegnazione di attributi di tipo file a un ProgID associato consente di controllare alcuni aspetti del comportamento del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c685d-104">Assigning file type attributes to an associated ProgID enables you to control some aspects of the file type's behavior.</span></span> <span data-ttu-id="c685d-105">Prima di Windows Vista, questi attributi potevano consentire di limitare la portata a cui l'utente può utilizzare la scheda delle proprietà **Opzioni cartella** per modificare diversi aspetti del tipo di file, ad esempio l'icona o i verbi.</span><span class="sxs-lookup"><span data-stu-id="c685d-105">Prior to Windows Vista, these attributes could enable you to limit the extent to which the user could use the **Folder Options** property tab to modify various aspects of the file type, such as its icon or verbs.</span></span>

<span data-ttu-id="c685d-106">Gli attributi del tipo di file sono flag binari specificati come **reg \_ DWORD** o valori **\_ binari reg** nella sottochiave ProgID associata al tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c685d-106">File type attributes are binary flags specified as **REG\_DWORD** or **REG\_BINARY** values in the file type's associated ProgID subkey.</span></span>

<span data-ttu-id="c685d-107">Per assegnare attributi per un tipo di file, attenersi alla seguente procedura.</span><span class="sxs-lookup"><span data-stu-id="c685d-107">To assign attributes for a file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="c685d-108">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c685d-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="c685d-109">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="c685d-109">Step 1:</span></span>

<span data-ttu-id="c685d-110">Aggiungere una voce flag alla sottochiave ProgID associata al tipo di file.</span><span class="sxs-lookup"><span data-stu-id="c685d-110">Add an EditFlags entry to the file type's associated ProgID subkey.</span></span>

### <a name="step-2"></a><span data-ttu-id="c685d-111">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="c685d-111">Step 2:</span></span>

<span data-ttu-id="c685d-112">Impostare la voce sul valore dell'attributo appropriato.</span><span class="sxs-lookup"><span data-stu-id="c685d-112">Set the entry to the appropriate attribute value.</span></span>

<span data-ttu-id="c685d-113">Nell'esempio seguente vengono illustrati gli \_ attributi di FTA NoRemove (0x00000010) e FTA \_ NoNewVerb (0x00000020) impostati per il tipo di file con estensione MYP.</span><span class="sxs-lookup"><span data-stu-id="c685d-113">The following example shows the FTA\_NoRemove (0x00000010) and FTA\_NoNewVerb (0x00000020) attributes set for the .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a><span data-ttu-id="c685d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c685d-114">Remarks</span></span>

<span data-ttu-id="c685d-115">I flag possono essere combinati con un OR logico per formare il singolo valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="c685d-115">The flags can be combined with a logical OR to form the single attribute value.</span></span>

<span data-ttu-id="c685d-116">Per un elenco di possibili attributi dei tipi di file e dei relativi valori esadecimali e altri dettagli su come recuperare e impostare a livello di codice questi valori, vedere [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span><span class="sxs-lookup"><span data-stu-id="c685d-116">For a list of possible file type attributes and their hexadecimal values, and more details on programmatically retrieving and setting these values, see [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span></span>

 

 



