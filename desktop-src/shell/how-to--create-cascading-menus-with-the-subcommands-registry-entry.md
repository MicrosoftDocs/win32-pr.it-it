---
description: In Windows 7 e versioni successive, è possibile usare la voce sottocomandi nel registro di sistema per creare menu a cascata usando la procedura descritta in questo argomento.
title: Creare menu a cascata con la voce del registro di sistema sottocomandi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b1168daae5ea927f079c66eb436c099f8b3d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994693"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="0f4a0-103">Come creare menu a cascata con la voce del registro di sistema sottocomandi</span><span class="sxs-lookup"><span data-stu-id="0f4a0-103">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="0f4a0-104">In Windows 7 e versioni successive, è possibile usare la voce sottocomandi nel registro di sistema per creare menu a cascata usando la procedura descritta in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="0f4a0-104">In Windows 7 and later, you can use the SubCommands entry in the registry to create cascading menus by using the procedure given in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="0f4a0-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="0f4a0-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="0f4a0-106">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="0f4a0-106">Step 1:</span></span>

<span data-ttu-id="0f4a0-107">Creare una nuova sottochiave in **HKEY \_ classi \_ radice** \\ *ProgID* \\ **Shell**, dove *ProgID* è il tipo di file per cui si vuole aggiungere un menu a cascata.</span><span class="sxs-lookup"><span data-stu-id="0f4a0-107">Create a new subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**, where *ProgID* is the file type for which you want to add a cascading menu.</span></span> <span data-ttu-id="0f4a0-108">È possibile assegnare alla nuova sottochiave un nome qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="0f4a0-108">You can name this new subkey anything you'd like.</span></span> <span data-ttu-id="0f4a0-109">Nella parte restante di questo argomento verrà chiamato *CascadeMenu*, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="0f4a0-109">For the remainder of this topic, we'll call it *CascadeMenu*, as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a><span data-ttu-id="0f4a0-110">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="0f4a0-110">Step 2:</span></span>

<span data-ttu-id="0f4a0-111">Aggiungere una voce denominata "MUIVerb", di tipo **reg \_ SZ** o **reg \_ expand \_ SZ**, alla sottochiave *CascadeMenu* .</span><span class="sxs-lookup"><span data-stu-id="0f4a0-111">Add an entry named "MUIVerb", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="0f4a0-112">Assegnare a questa voce un valore stringa, ad esempio "menu test Cascade".</span><span class="sxs-lookup"><span data-stu-id="0f4a0-112">Assign this entry a string value such as "Test Cascade Menu".</span></span> <span data-ttu-id="0f4a0-113">In genere, questa stringa viene fornita come riferimento a una risorsa nel formato " @file , Resource".</span><span class="sxs-lookup"><span data-stu-id="0f4a0-113">Normally, this string is provided as a resource reference in the form "@file, resource".</span></span> <span data-ttu-id="0f4a0-114">Il valore (predefinito) per la sottochiave *CascadeMenu* non deve essere impostato.</span><span class="sxs-lookup"><span data-stu-id="0f4a0-114">The (Default) value for the *CascadeMenu* subkey should not be set.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a><span data-ttu-id="0f4a0-115">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="0f4a0-115">Step 3:</span></span>

<span data-ttu-id="0f4a0-116">Aggiungere una voce denominata "subcommands", di tipo **reg \_ SZ** o **reg \_ expand \_ SZ**, alla sottochiave *CascadeMenu* .</span><span class="sxs-lookup"><span data-stu-id="0f4a0-116">Add an entry named "SubCommands", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="0f4a0-117">Assegnare a questa voce un elenco delimitato da punti e virgola dei verbi che devono essere visualizzati nel menu, nell'ordine di visualizzazione desiderato.</span><span class="sxs-lookup"><span data-stu-id="0f4a0-117">Assign this entry a semicolon-delimited list of the verbs that should appear on the menu, in their desired order of appearance.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a><span data-ttu-id="0f4a0-118">Passaggio 4:</span><span class="sxs-lookup"><span data-stu-id="0f4a0-118">Step 4:</span></span>

<span data-ttu-id="0f4a0-119">Popolare la sottochiave **CommandStore** con le implementazioni dei verbi per tutti i metodi di implementazione di verbi statici personalizzati usati nella voce dei sottocomandi. Per esempio:</span><span class="sxs-lookup"><span data-stu-id="0f4a0-119">Populate the **CommandStore** subkey with verb implementations for any custom static verb implementation methods that you've used in your SubCommands entry; for example:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  CommandStore
                     Shell
                        VerbName
                           command
                              (Default) = notepad.exe %1
```

## <a name="related-topics"></a><span data-ttu-id="0f4a0-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f4a0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f4a0-121">Creazione di menu a cascata statici</span><span class="sxs-lookup"><span data-stu-id="0f4a0-121">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
</dt> </dl>

 

 



