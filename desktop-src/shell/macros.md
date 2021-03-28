---
description: In questa sezione vengono descritte le macro di utilità della shell di Windows.
title: Macro della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5be120f4-bf5d-44b3-b508-20a2104655fa
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 085bca918cfa6ca1441272c3c9181226ef603ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967754"
---
# <a name="shell-macros"></a><span data-ttu-id="aa9e7-103">Macro della shell</span><span class="sxs-lookup"><span data-stu-id="aa9e7-103">Shell Macros</span></span>

<span data-ttu-id="aa9e7-104">In questa sezione vengono descritte le macro di utilità della shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="aa9e7-104">This section describes the Windows Shell utility macros.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aa9e7-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="aa9e7-105">In this section</span></span>



| <span data-ttu-id="aa9e7-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="aa9e7-106">Topic</span></span>                                                                  | <span data-ttu-id="aa9e7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa9e7-107">Description</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa9e7-108">**DEFINIRE \_ PropertyKey**</span><span class="sxs-lookup"><span data-stu-id="aa9e7-108">**DEFINE\_PROPERTYKEY**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-define_propertykey)<br/>           | <span data-ttu-id="aa9e7-109">Usato per comprimere un identificatore di formato (FMTID) e un identificatore di proprietà (PID) in una struttura [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) che rappresenta una chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="aa9e7-109">Used to pack a format identifier (FMTID) and property identifier (PID) into a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure that represents a property key.</span></span><br/>                                                                                    |
| [<span data-ttu-id="aa9e7-110">**argomenti di IID \_ PPV \_**</span><span class="sxs-lookup"><span data-stu-id="aa9e7-110">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)<br/>                      | <span data-ttu-id="aa9e7-111">Utilizzato per recuperare un puntatore a interfaccia, fornendo automaticamente il valore IID dell'interfaccia richiesta in base al tipo del puntatore a interfaccia utilizzato.</span><span class="sxs-lookup"><span data-stu-id="aa9e7-111">Used to retrieve an interface pointer, supplying the IID value of the requested interface automatically based on the type of the interface pointer used.</span></span> <span data-ttu-id="aa9e7-112">In questo modo si evita un errore di codifica comune controllando il tipo del valore passato in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="aa9e7-112">This avoids a common coding error by checking the type of the value passed at compile time.</span></span><br/> |
| [<span data-ttu-id="aa9e7-113">**IsEqualPropertyKey**</span><span class="sxs-lookup"><span data-stu-id="aa9e7-113">**IsEqualPropertyKey**</span></span>](/windows/desktop/api/Propkeydef/nf-propkeydef-isequalpropertykey)<br/>            | <span data-ttu-id="aa9e7-114">Confronta i membri di due strutture [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) e restituisce un valore che indica se sono uguali.</span><span class="sxs-lookup"><span data-stu-id="aa9e7-114">Compares the members of two [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structures and returns whether they are equal.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="aa9e7-115">**MAKEDLLVERULL**</span><span class="sxs-lookup"><span data-stu-id="aa9e7-115">**MAKEDLLVERULL**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull)<br/>                      | <span data-ttu-id="aa9e7-116">Usato per comprimere le informazioni sulla versione della DLL in un valore ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="aa9e7-116">Used to pack DLL version information into a ULONGLONG value.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="aa9e7-117">**\_DisplayErrorTip NetAddr**</span><span class="sxs-lookup"><span data-stu-id="aa9e7-117">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)<br/> | <span data-ttu-id="aa9e7-118">Visualizza un messaggio di errore nel fumetto suggerimento associato al controllo dell'indirizzo di rete.</span><span class="sxs-lookup"><span data-stu-id="aa9e7-118">Displays an error message in the balloon tip associated with the network address control.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="aa9e7-119">**NetAddr \_ GetAddress**</span><span class="sxs-lookup"><span data-stu-id="aa9e7-119">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)<br/>           | <span data-ttu-id="aa9e7-120">Indica se un indirizzo di rete è conforme a un tipo e un formato specificati.</span><span class="sxs-lookup"><span data-stu-id="aa9e7-120">Indicates whether a network address conforms to a specified type and format.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="aa9e7-121">**\_GetAllowType NetAddr**</span><span class="sxs-lookup"><span data-stu-id="aa9e7-121">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)<br/>       | <span data-ttu-id="aa9e7-122">Recupera i tipi di indirizzi di rete accettati da un controllo di indirizzo di rete specificato.</span><span class="sxs-lookup"><span data-stu-id="aa9e7-122">Retrieves the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="aa9e7-123">**\_SetAllowType NetAddr**</span><span class="sxs-lookup"><span data-stu-id="aa9e7-123">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)<br/>       | <span data-ttu-id="aa9e7-124">Imposta i tipi di indirizzi di rete accettati da un controllo di indirizzo di rete specificato.</span><span class="sxs-lookup"><span data-stu-id="aa9e7-124">Sets the network address types that a specified network address control accepts.</span></span><br/>                                                                                                                                                                     |



 

 

 
