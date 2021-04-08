---
title: Intestazione ACF
description: L'intestazione ACF contiene attributi specifici della piattaforma che si applicano all'interfaccia nel suo complesso. Gli attributi applicati a singoli tipi e funzioni nel corpo di ACF eseguono l'override degli attributi nell'intestazione ACF. Nessun attributo obbligatorio nell'intestazione ACF.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047023"
---
# <a name="the-acf-header"></a><span data-ttu-id="50cdb-105">Intestazione ACF</span><span class="sxs-lookup"><span data-stu-id="50cdb-105">The ACF Header</span></span>

<span data-ttu-id="50cdb-106">L'intestazione ACF contiene attributi specifici della piattaforma che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="50cdb-106">The ACF header contains platform-specific attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="50cdb-107">Gli attributi applicati a singoli tipi e funzioni nel corpo di ACF eseguono l'override degli attributi nell'intestazione ACF.</span><span class="sxs-lookup"><span data-stu-id="50cdb-107">Attributes applied to individual types and functions in the ACF body override the attributes in the ACF header.</span></span> <span data-ttu-id="50cdb-108">Nessun attributo obbligatorio nell'intestazione ACF.</span><span class="sxs-lookup"><span data-stu-id="50cdb-108">No attributes are required in the ACF header.</span></span>

<span data-ttu-id="50cdb-109">L'intestazione ACF può includere uno degli attributi seguenti: **\[** [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) **\]** , **\[** [**\_ handle implicito**](/windows/desktop/Midl/implicit-handle) **\]** o [**\_ handle esplicito**](/windows/desktop/Midl/explicit-handle) **\]** .</span><span class="sxs-lookup"><span data-stu-id="50cdb-109">The ACF header can include one of the following attributes: **\[**[**auto\_handle**](/windows/desktop/Midl/auto-handle)**\]**, **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]**, or [**explicit\_handle**](/windows/desktop/Midl/explicit-handle)**\]**.</span></span> <span data-ttu-id="50cdb-110">Se viene utilizzato l'handle **\[ automatico \_ \]** o l' **\[ \_ handle \] implicito** , viene specificato il tipo di handle di associazione che verrà utilizzato per l'associazione quando una funzione remota non dispone di un parametro di handle di binding esplicito.</span><span class="sxs-lookup"><span data-stu-id="50cdb-110">If **\[auto\_handle\]** or **\[implicit\_handle\]** is used, it specifies the type of binding handle that will be used for binding when a remote function does not have an explicit binding-handle parameter.</span></span> <span data-ttu-id="50cdb-111">Quando ACF non è presente o non specifica un handle di binding automatico, implicito o esplicito, MIDL usa l' **\[ \_ handle \] automatico** per l'associazione implicita.</span><span class="sxs-lookup"><span data-stu-id="50cdb-111">When the ACF is not present or does not specify an automatic, implicit, or explicit binding handle, MIDL uses **\[auto\_handle\]** for implicit binding.</span></span>

<span data-ttu-id="50cdb-112">Il **\[** [**codice**](/windows/desktop/Midl/code) **\]** o **\[** [**NoCode**](/windows/desktop/Midl/nocode) **\]** può essere visualizzato nell'intestazione dell'interfaccia, ma quello scelto può apparire una sola volta.</span><span class="sxs-lookup"><span data-stu-id="50cdb-112">Either **\[**[**code**](/windows/desktop/Midl/code)**\]** or **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]** can appear in the interface header, but the one you choose can appear only once.</span></span> <span data-ttu-id="50cdb-113">Quando nessuno degli attributi è presente, il compilatore usa il **\[ codice \]** come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="50cdb-113">When neither attribute is present, the compiler uses **\[code\]** as a default.</span></span>

<span data-ttu-id="50cdb-114">Per altre informazioni, vedere [attributi ACF](/windows/desktop/Midl/acf-attributes).</span><span class="sxs-lookup"><span data-stu-id="50cdb-114">For more information, see [ACF Attributes](/windows/desktop/Midl/acf-attributes).</span></span>

 

 