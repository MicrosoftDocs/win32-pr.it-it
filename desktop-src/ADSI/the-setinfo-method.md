---
title: Metodo seinfo
description: Il metodo IADs SetInfo Salva i valori correnti per le proprietà di questo oggetto Active Directory dalla cache delle proprietà nell'archivio directory sottostante. Questo è analogo allo scaricamento di un buffer su disco.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- SetInfo ADSI, uso
- Proprietà ADSI, salvare i valori correnti per le proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5965a46e5accd2a00adc006fe37511de13ff0df3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328348"
---
# <a name="the-setinfo-method"></a><span data-ttu-id="77e36-106">Metodo seinfo</span><span class="sxs-lookup"><span data-stu-id="77e36-106">The SetInfo Method</span></span>

<span data-ttu-id="77e36-107">Il metodo [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) Salva i valori correnti per le proprietà di questo oggetto Active Directory dalla cache delle proprietà nell'archivio directory sottostante.</span><span class="sxs-lookup"><span data-stu-id="77e36-107">The [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method saves the current values for the properties for this Active Directory object from the property cache to the underlying directory store.</span></span> <span data-ttu-id="77e36-108">Questo è analogo allo scaricamento di un buffer su disco.</span><span class="sxs-lookup"><span data-stu-id="77e36-108">This is analogous to flushing a buffer out to disk.</span></span>

<span data-ttu-id="77e36-109">Per aggiornare gli oggetti già presenti nella directory, è necessario creare una nuova voce di directory [**per gli oggetti**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) appena creati.</span><span class="sxs-lookup"><span data-stu-id="77e36-109">[**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) updates objects that already exist in the directory, or create a new directory entry for newly created objects.</span></span>

<span data-ttu-id="77e36-110">Al momento della chiamata a [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , se i valori della cache delle proprietà sono stati scritti con un codice di controllo [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) , ad esempio \_ l'aggiornamento delle proprietà Ads \_ o \_ la proprietà Ads \_ Clear, le richieste appropriate vengono passate al servizio directory sottostante.</span><span class="sxs-lookup"><span data-stu-id="77e36-110">At the time of the [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) call, if any property cache values have been written with a [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) control code, such as ADS\_PROPERTY\_UPDATE or ADS\_PROPERTY\_CLEAR, then the appropriate requests are passed on to the underlying directory service.</span></span>

 

 




