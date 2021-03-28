---
description: È possibile testare i valori del flag SFGAO degli attributi della Shell per un elemento per determinare se il verbo deve essere abilitato o disabilitato.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Come usare gli attributi degli elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881557"
---
# <a name="how-to-use-item-attributes"></a><span data-ttu-id="4bd3c-103">Come usare gli attributi degli elementi</span><span class="sxs-lookup"><span data-stu-id="4bd3c-103">How to Use Item Attributes</span></span>

<span data-ttu-id="4bd3c-104">È possibile testare i valori del flag [**SFGAO**](sfgao.md) degli attributi della Shell per un elemento per determinare se il verbo deve essere abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4bd3c-104">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="4bd3c-105">Per usare questa funzionalità di attributo, aggiungere i seguenti valori **reg \_ DWORD** sotto il verbo:</span><span class="sxs-lookup"><span data-stu-id="4bd3c-105">To use this attribute feature, add the following **REG\_DWORD** values under the verb:</span></span>

## <a name="instructions"></a><span data-ttu-id="4bd3c-106">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="4bd3c-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="4bd3c-107">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="4bd3c-107">Step 1:</span></span>

<span data-ttu-id="4bd3c-108">Il valore AttributeMask specifica il valore [**SFGAO**](sfgao.md) dei valori di bit della maschera con cui eseguire il test.</span><span class="sxs-lookup"><span data-stu-id="4bd3c-108">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>

### <a name="step-2"></a><span data-ttu-id="4bd3c-109">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="4bd3c-109">Step 2:</span></span>

<span data-ttu-id="4bd3c-110">Il valore AttributeValue specifica il valore [**SFGAO**](sfgao.md) dei bit sottoposti a test.</span><span class="sxs-lookup"><span data-stu-id="4bd3c-110">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="4bd3c-111">Passaggio 3:</span><span class="sxs-lookup"><span data-stu-id="4bd3c-111">Step 3:</span></span>

<span data-ttu-id="4bd3c-112">ImpliedSelectionModel specifica zero per i verbi di elemento o un valore diverso da zero per i verbi nel menu di scelta rapida in background.</span><span class="sxs-lookup"><span data-stu-id="4bd3c-112">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bd3c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bd3c-113">Remarks</span></span>

<span data-ttu-id="4bd3c-114">Nell'esempio seguente di voce del registro di sistema, AttributeMask è impostato su [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="4bd3c-114">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



