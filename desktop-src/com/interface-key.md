---
title: Chiave interfaccia
description: Registra le nuove interfacce associando il nome di un'interfaccia a un ID di interfaccia (IID). Deve essere presente una sottochiave IID per ogni nuova interfaccia.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Chiave del registro di sistema Interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045073"
---
# <a name="interface-key"></a><span data-ttu-id="5ff50-105">Chiave interfaccia</span><span class="sxs-lookup"><span data-stu-id="5ff50-105">Interface Key</span></span>

<span data-ttu-id="5ff50-106">Registra le nuove interfacce associando il nome di un'interfaccia a un ID di interfaccia (IID).</span><span class="sxs-lookup"><span data-stu-id="5ff50-106">Registers new interfaces by associating an interface name with an interface ID (IID).</span></span> <span data-ttu-id="5ff50-107">Deve essere presente una sottochiave IID per ogni nuova interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5ff50-107">There must be one IID subkey for each new interface.</span></span>

## <a name="registry-key"></a><span data-ttu-id="5ff50-108">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="5ff50-108">Registry Key</span></span>

<span data-ttu-id="5ff50-109">**HKEY \_ \_Interfaccia delle \\ \\ classi software \\ del computer locale** \\ *{* IID *}*</span><span class="sxs-lookup"><span data-stu-id="5ff50-109">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Interface**\\ *{* IID *}*</span></span>



| <span data-ttu-id="5ff50-110">Valore del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="5ff50-110">Registry value</span></span>                               | <span data-ttu-id="5ff50-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ff50-111">Description</span></span>                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ff50-112">**BaseInterface**</span><span class="sxs-lookup"><span data-stu-id="5ff50-112">**BaseInterface**</span></span>](baseinterface.md)       | <span data-ttu-id="5ff50-113">Identifica l'interfaccia da cui deriva l'interfaccia corrente.</span><span class="sxs-lookup"><span data-stu-id="5ff50-113">Identifies the interface from which the current interface is derived.</span></span>                                  |
| [<span data-ttu-id="5ff50-114">**NumMethods**</span><span class="sxs-lookup"><span data-stu-id="5ff50-114">**NumMethods**</span></span>](nummethods.md)             | <span data-ttu-id="5ff50-115">Contiene il numero di metodi nell'interfaccia associata, inclusi i metodi delle interfacce derivate.</span><span class="sxs-lookup"><span data-stu-id="5ff50-115">Contains the number of methods in the associated interface, including methods from derived interfaces.</span></span> |
| [<span data-ttu-id="5ff50-116">**ProxyStubClsid**</span><span class="sxs-lookup"><span data-stu-id="5ff50-116">**ProxyStubClsid**</span></span>](proxystubclsid.md)     | <span data-ttu-id="5ff50-117">Esegue il mapping di un IID a un CLSID nelle DLL proxy a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="5ff50-117">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>                                                           |
| [<span data-ttu-id="5ff50-118">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="5ff50-118">**ProxyStubClsid32**</span></span>](proxystubclsid32.md) | <span data-ttu-id="5ff50-119">Esegue il mapping di un IID a un CLSID in DLL proxy a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="5ff50-119">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="5ff50-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ff50-120">Remarks</span></span>

<span data-ttu-id="5ff50-121">La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.</span><span class="sxs-lookup"><span data-stu-id="5ff50-121">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ff50-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5ff50-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ff50-123">**Interfaccia**</span><span class="sxs-lookup"><span data-stu-id="5ff50-123">**Interface**</span></span>](interface.md)
</dt> </dl>

 

 




