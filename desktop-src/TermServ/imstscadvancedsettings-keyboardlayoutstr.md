---
title: Proprietà KeyBoardLayoutStr di IMsTscAdvancedSettings
description: Specifica il nome dell'identificatore delle impostazioni locali di input attivo (denominato in precedenza il layout della tastiera) da usare per la connessione.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà KeyBoardLayoutStr
- Servizi Desktop remoto proprietà KeyBoardLayoutStr, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà KeyBoardLayoutStr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741503"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a><span data-ttu-id="57ba2-106">Proprietà IMsTscAdvancedSettings:: KeyBoardLayoutStr</span><span class="sxs-lookup"><span data-stu-id="57ba2-106">IMsTscAdvancedSettings::KeyBoardLayoutStr property</span></span>

<span data-ttu-id="57ba2-107">Specifica il nome dell'identificatore delle impostazioni locali di input attivo (denominato in precedenza il layout della tastiera) da usare per la connessione.</span><span class="sxs-lookup"><span data-stu-id="57ba2-107">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span>

<span data-ttu-id="57ba2-108">Se questa proprietà non è impostata, il controllo Usa il layout predefinito restituito dalla funzione [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) .</span><span class="sxs-lookup"><span data-stu-id="57ba2-108">If this property is not set, the control uses the default layout returned by the [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) function.</span></span>

<span data-ttu-id="57ba2-109">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="57ba2-109">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ba2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57ba2-110">Syntax</span></span>


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a><span data-ttu-id="57ba2-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="57ba2-111">Property value</span></span>

<span data-ttu-id="57ba2-112">Nome dell'identificatore delle impostazioni locali di input attivo.</span><span class="sxs-lookup"><span data-stu-id="57ba2-112">The name of the active input locale identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="57ba2-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="57ba2-113">Error codes</span></span>

<span data-ttu-id="57ba2-114">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="57ba2-114">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="57ba2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="57ba2-115">Remarks</span></span>

<span data-ttu-id="57ba2-116">La proprietà è un numero esadecimale a otto cifre in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="57ba2-116">The property is an eight digit hexadecimal number in string form.</span></span> <span data-ttu-id="57ba2-117">Le quattro cifre inferiori rappresentano l'identificatore della lingua e le quattro cifre più alte rappresentano la variazione della tastiera all'interno di tale lingua.</span><span class="sxs-lookup"><span data-stu-id="57ba2-117">The lower four digits represent the language identifier, and the upper four digits represent the keyboard variation within that language.</span></span> <span data-ttu-id="57ba2-118">Quindi, ad esempio, "00000409" rappresenterà la tastiera inglese (Stati Uniti) predefinita perché "0409" è l'identificatore della lingua inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="57ba2-118">So, for example, "00000409" would represent the default US English keyboard because "0409" is the US English language identifier.</span></span> <span data-ttu-id="57ba2-119">La variante Dvorak della tastiera inglese (Stati Uniti) ha un identificatore "00010409".</span><span class="sxs-lookup"><span data-stu-id="57ba2-119">The Dvorak variation of the US English keyboard has an identifier of "00010409".</span></span> <span data-ttu-id="57ba2-120">È possibile trovare i layout di tastiera disponibili, elencati in base agli identificatori del layout di tastiera, nel registro di sistema in</span><span class="sxs-lookup"><span data-stu-id="57ba2-120">You can find the available keyboard layouts, listed by their keyboard layout identifiers, in the registry under</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

<span data-ttu-id="57ba2-121">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="57ba2-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57ba2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57ba2-122">Requirements</span></span>



| <span data-ttu-id="57ba2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="57ba2-123">Requirement</span></span> | <span data-ttu-id="57ba2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="57ba2-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ba2-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57ba2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="57ba2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57ba2-126">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="57ba2-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57ba2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="57ba2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57ba2-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="57ba2-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="57ba2-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="57ba2-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57ba2-130"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="57ba2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="57ba2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57ba2-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57ba2-132"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="57ba2-133">IID</span><span class="sxs-lookup"><span data-stu-id="57ba2-133">IID</span></span><br/>                      | <span data-ttu-id="57ba2-134">IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="57ba2-134">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57ba2-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57ba2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ba2-136">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="57ba2-136">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

