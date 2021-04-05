---
description: Ogni proprietà del controllo di registrazione certificati è di lettura/scrittura e presenta un valore predefinito inizializzato nonché un set di valori accettabili.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Uso delle proprietà del controllo di registrazione certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753434"
---
# <a name="using-the-certificate-enrollment-control-properties"></a><span data-ttu-id="31a97-103">Uso delle proprietà del controllo di registrazione certificati</span><span class="sxs-lookup"><span data-stu-id="31a97-103">Using the Certificate Enrollment Control Properties</span></span>

<span data-ttu-id="31a97-104">Ogni proprietà del controllo di registrazione certificati è di lettura/scrittura e presenta un valore predefinito inizializzato nonché un set di valori accettabili.</span><span class="sxs-lookup"><span data-stu-id="31a97-104">Each Certificate Enrollment Control property is read/write and has an initialized default as well as a set of acceptable values.</span></span> <span data-ttu-id="31a97-105">È possibile impostare una proprietà su qualsiasi valore all'interno di questo set per modificare il comportamento dei metodi che utilizzano la proprietà.</span><span class="sxs-lookup"><span data-stu-id="31a97-105">You can set a property to any value within this set in order to modify the behavior of methods that use the property.</span></span> <span data-ttu-id="31a97-106">Per ottenere un comportamento desiderato, impostare la proprietà prima di chiamare il metodo che usa il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="31a97-106">To get a desired behavior, set the property before you call the method that uses that property's value.</span></span>

<span data-ttu-id="31a97-107">Si noti, tuttavia, che dopo la chiamata dei metodi seguenti</span><span class="sxs-lookup"><span data-stu-id="31a97-107">Note, however, that after calling the following methods</span></span>

-   [<span data-ttu-id="31a97-108">**acceptPKCS7**</span><span class="sxs-lookup"><span data-stu-id="31a97-108">**acceptPKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [<span data-ttu-id="31a97-109">**acceptFilePKCS7**</span><span class="sxs-lookup"><span data-stu-id="31a97-109">**acceptFilePKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [<span data-ttu-id="31a97-110">**createPKCS10**</span><span class="sxs-lookup"><span data-stu-id="31a97-110">**createPKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [<span data-ttu-id="31a97-111">**createFilePKCS10**</span><span class="sxs-lookup"><span data-stu-id="31a97-111">**createFilePKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

<span data-ttu-id="31a97-112">le proprietà seguenti sono bloccate dalla reimpostazione</span><span class="sxs-lookup"><span data-stu-id="31a97-112">the following properties are blocked from being reset</span></span>

-   [<span data-ttu-id="31a97-113">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="31a97-113">**ProviderType**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [<span data-ttu-id="31a97-114">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="31a97-114">**KeySpec**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [<span data-ttu-id="31a97-115">**ProviderFlags**</span><span class="sxs-lookup"><span data-stu-id="31a97-115">**ProviderFlags**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [<span data-ttu-id="31a97-116">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="31a97-116">**ContainerName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [<span data-ttu-id="31a97-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="31a97-117">**ProviderName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

<span data-ttu-id="31a97-118">a meno che non venga chiamato il metodo [**ICEnroll4:: Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) .</span><span class="sxs-lookup"><span data-stu-id="31a97-118">unless the [**ICEnroll4::Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) method is called.</span></span>

<span data-ttu-id="31a97-119">Per informazioni sui singoli metodi e proprietà, vedere gli argomenti di riferimento relativi a tali proprietà e metodi nel [riferimento alla crittografia](cryptography-reference.md).</span><span class="sxs-lookup"><span data-stu-id="31a97-119">For information about individual properties and methods, see the reference topics for those properties and methods in the [Cryptography Reference](cryptography-reference.md).</span></span>

<span data-ttu-id="31a97-120">Le sezioni seguenti contengono informazioni specifiche della lingua per l'impostazione e il recupero delle proprietà del controllo di registrazione certificati:</span><span class="sxs-lookup"><span data-stu-id="31a97-120">The following sections contain language-specific information for setting and retrieving the Certificate Enrollment Control properties:</span></span>

-   [<span data-ttu-id="31a97-121">Proprietà del controllo di registrazione certificati in C++</span><span class="sxs-lookup"><span data-stu-id="31a97-121">Certificate Enrollment Control Properties in C++</span></span>](certificate-enrollment-control-properties-in-c-.md)

 

 
