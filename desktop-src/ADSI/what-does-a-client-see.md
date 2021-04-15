---
title: Che cosa Visualizza un client
description: In questo argomento vengono elencati i modi in cui un client Visualizza i dati ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, che cosa Visualizza un client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517109"
---
# <a name="what-does-a-client-see"></a><span data-ttu-id="b3f70-104">Che cosa Visualizza un client?</span><span class="sxs-lookup"><span data-stu-id="b3f70-104">What Does a Client See?</span></span>

-   <span data-ttu-id="b3f70-105">Un client visualizza ADSI e tutti i relativi oggetti di estensione come un unico oggetto.</span><span class="sxs-lookup"><span data-stu-id="b3f70-105">A client sees ADSI and all of its extension objects as one object.</span></span>
-   <span data-ttu-id="b3f70-106">Un client ADSI rileva un'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che gestisce tutte le interfacce dual e dispatch nell'oggetto, indipendentemente dal fatto che l'interfaccia duale o dispatch venga implementata da Aggregator nel provider o da un'estensione.</span><span class="sxs-lookup"><span data-stu-id="b3f70-106">An ADSI client sees one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface that handles all the dual and dispatch interfaces in the object, whether the dual or dispatch interface is implemented by the aggregator in the provider or by an extension.</span></span> <span data-ttu-id="b3f70-107">Vedere [risoluzione dei conflitti di nomi di funzione/proprietà in automazione nelle estensioni](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="b3f70-107">Please see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>
-   <span data-ttu-id="b3f70-108">ADSI non espone informazioni sui tipi tramite i metodi [**IDispatch:: GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) o [**IDispatch:: GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) .</span><span class="sxs-lookup"><span data-stu-id="b3f70-108">ADSI does not expose any type information through the [**IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) or [**IDispatch::GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) methods.</span></span> <span data-ttu-id="b3f70-109">ADSI fornisce informazioni sul tipo tramite la libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="b3f70-109">ADSI provides type information through the type library.</span></span>

 

 