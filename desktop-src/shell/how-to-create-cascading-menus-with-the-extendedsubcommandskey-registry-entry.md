---
description: In Windows 7 e versioni successive, è possibile usare la sottochiave ExtendedSubCommandsKey per creare menu a cascata estesi.
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: Creare menu a cascata con la voce del registro di sistema ExtendedSubCommandsKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756515"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="f685c-103">Come creare menu a cascata con la voce del registro di sistema ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="f685c-103">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="f685c-104">In Windows 7 e versioni successive, è possibile usare la sottochiave **ExtendedSubCommandsKey** per creare menu a cascata estesi.</span><span class="sxs-lookup"><span data-stu-id="f685c-104">In Windows 7 and later, you can use the **ExtendedSubCommandsKey** subkey to create extended cascading menus.</span></span>

<span data-ttu-id="f685c-105">Lo screenshot seguente è un esempio di menu a cascata esteso.</span><span class="sxs-lookup"><span data-stu-id="f685c-105">The following screen shot is an example of an extended cascading menu.</span></span>

![screenshot che mostra il menu a cascata esteso per i dispositivi](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="f685c-107">Poiché **la \_ \_ radice delle classi HKEY** è una combinazione di **HKEY \_ Current \_ User** e **HKEY \_ Local \_ computer**, è possibile registrare i sottoverbi nella sottochiave **HKEY \_ Current \_ User** \\  \\ **Classes** .</span><span class="sxs-lookup"><span data-stu-id="f685c-107">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register the subverbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="f685c-108">Il vantaggio di questa operazione è che non è necessaria l'autorizzazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="f685c-108">The advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="f685c-109">Altre associazioni di file possono riutilizzare l'intero set di verbi specificando la stessa sottochiave **ExtendedSubCommandsKey** .</span><span class="sxs-lookup"><span data-stu-id="f685c-109">Other file associations can reuse this entire set of verbs by specifying the same **ExtendedSubCommandsKey** subkey.</span></span> <span data-ttu-id="f685c-110">Se non è necessario riutilizzare questo set di verbi, è possibile elencare i verbi sotto l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="f685c-110">If you do not need to reuse this set of verbs, you can list the verbs under the parent.</span></span> <span data-ttu-id="f685c-111">In questo caso, assicurarsi che il valore predefinito dell'elemento padre sia vuoto, come illustrato nell'esempio di voce del registro di sistema in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="f685c-111">In this case, make sure the default value of the parent is empty, as illustrated in the registry entry example in this section.</span></span>

## <a name="instructions"></a><span data-ttu-id="f685c-112">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="f685c-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="f685c-113">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="f685c-113">Step 1:</span></span>

<span data-ttu-id="f685c-114">Creare una sottochiave in **HKEY \_ classi \_ radice** \\ *ProgID* \\ **Shell** \\ *CascadeMenuKey* e assegnare a CascadeMenuKey un nome come *CascadeTest*, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="f685c-114">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**\\*CascadeMenuKey* and give the CascadeMenuKey a name such as *CascadeTest*, for example.</span></span> <span data-ttu-id="f685c-115">Aggiungere quindi una voce MUIVerb di tipo **reg \_ SZ** e assegnarle un nome, ad esempio test Cascade menu 2, come illustrato nell'esempio di registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="f685c-115">Then add a MUIVerb entry of **REG\_SZ** type and give it a name such as Test Cascade Menu 2, as illustrated in the following registry example.</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a><span data-ttu-id="f685c-116">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="f685c-116">Step 2:</span></span>

<span data-ttu-id="f685c-117">Nella sottochiave *CascadeTest* creata aggiungere una sottochiave **ExtendedSubCommandsKey** e quindi aggiungere il documento sottocomandi (di tipo **reg \_ SZ**), ad esempio:</span><span class="sxs-lookup"><span data-stu-id="f685c-117">Under the *CascadeTest* subkey that you created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of type **REG\_SZ**); for example:</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Layout
               Properties
               Select all
```

<span data-ttu-id="f685c-118">Verificare che il valore predefinito della sottochiave del *menu 2 di test Cascade* sia vuoto e visualizzato come **(valore non impostato)**.</span><span class="sxs-lookup"><span data-stu-id="f685c-118">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

### <a name="step-3"></a><span data-ttu-id="f685c-119">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="f685c-119">Step 3:</span></span>

<span data-ttu-id="f685c-120">Popolare i sottoverbi utilizzando una delle seguenti implementazioni di verbi statici.</span><span class="sxs-lookup"><span data-stu-id="f685c-120">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="f685c-121">Si noti che la sottochiave CommandFlags rappresenta i valori EXPCMDFLAGS.</span><span class="sxs-lookup"><span data-stu-id="f685c-121">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="f685c-122">Se si desidera aggiungere un separatore prima o dopo la voce di menu a cascata, utilizzare ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40).</span><span class="sxs-lookup"><span data-stu-id="f685c-122">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="f685c-123">Per una descrizione di questi flag di Windows 7 e versioni successive, vedere [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="f685c-123">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="f685c-124">ECF \_ SEPARATORBEFORE funziona solo per le voci di menu di primo livello.</span><span class="sxs-lookup"><span data-stu-id="f685c-124">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="f685c-125">MUIVerb è di tipo **reg \_ SZ** e CommandFlags è di tipo **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f685c-125">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Shell
                  cmd1
                     MUIVerb = Notepad
                     command
                        (Default) = %SystemRoot%\system32\notepad.exe %1
                  cmd2
                     MUIVerb = Wordpad
                     CommandFlags = 0x20
                     command
                        (Default) = C:\Program Files\Windows NT\Accessories\wordpad.exe %1
```

## <a name="remarks"></a><span data-ttu-id="f685c-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="f685c-126">Remarks</span></span>

<span data-ttu-id="f685c-127">Lo screenshot seguente illustra i precedenti esempi di voci della chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f685c-127">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![screenshot che mostra un esempio di menu a cascata che mostra le scelte del blocco note e di WordPad](images/file-assoc/testcascademenu2.png)

 

 



