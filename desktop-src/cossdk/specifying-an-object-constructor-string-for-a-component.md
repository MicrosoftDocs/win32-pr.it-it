---
description: Specifica di una stringa del costruttore di oggetti per un componente
ms.assetid: 0c5aaaae-368e-4b3e-a483-b3a23c353e6e
title: Specifica di una stringa del costruttore di oggetti per un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca4604d07a5b750d02a968456d33c9e5bc6bee8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877618"
---
# <a name="specifying-an-object-constructor-string-for-a-component"></a><span data-ttu-id="6e98f-103">Specifica di una stringa del costruttore di oggetti per un componente</span><span class="sxs-lookup"><span data-stu-id="6e98f-103">Specifying an Object Constructor String for a Component</span></span>

<span data-ttu-id="6e98f-104">Per specificare una stringa del costruttore di oggetti per un componente, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="6e98f-104">To specify an object constructor string for a component, use the following steps:</span></span>

1.  <span data-ttu-id="6e98f-105">Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="6e98f-105">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>
2.  <span data-ttu-id="6e98f-106">Nella finestra di dialogo Proprietà componente fare clic sulla scheda **attivazione** .</span><span class="sxs-lookup"><span data-stu-id="6e98f-106">In the component properties dialog box, click the **Activation** tab.</span></span>
3.  <span data-ttu-id="6e98f-107">Per abilitare l'uso della stringa del costruttore dell'oggetto, selezionare la casella di controllo **Abilita costruzione dell'oggetto** .</span><span class="sxs-lookup"><span data-stu-id="6e98f-107">To enable use of the object constructor string, select the **Enable object construction** check box.</span></span>
4.  <span data-ttu-id="6e98f-108">Nella casella **stringa costruttore** immettere la stringa di costruzione, ad esempio DSN = AccountingServer.</span><span class="sxs-lookup"><span data-stu-id="6e98f-108">In the **Constructor string** box, enter the construction string (for example, DSN=AccountingServer).</span></span> <span data-ttu-id="6e98f-109">È possibile immettere una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="6e98f-109">You have the option of entering an empty string.</span></span>

> [!Note]  
> <span data-ttu-id="6e98f-110">Le stringhe del costruttore di oggetti non devono essere usate per archiviare informazioni sensibili alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6e98f-110">Object constructor strings should not be used to store security-sensitive information.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6e98f-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6e98f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e98f-112">Concetti relativi alle stringhe del costruttore di oggetti COM+</span><span class="sxs-lookup"><span data-stu-id="6e98f-112">COM+ Object Constructor Strings Concepts</span></span>](com--object-constructor-strings-concepts.md)
</dt> <dt>

[<span data-ttu-id="6e98f-113">Uso di una stringa del costruttore di oggetti per costruire un componente</span><span class="sxs-lookup"><span data-stu-id="6e98f-113">Using an Object Constructor String to Construct a Component</span></span>](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



