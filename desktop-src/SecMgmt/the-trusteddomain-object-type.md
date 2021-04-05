---
description: I sistemi basati su Windows possono avere più istanze del tipo di oggetto TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: Tipo di oggetto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750858"
---
# <a name="the-trusteddomain-object-type"></a><span data-ttu-id="ae6d5-103">Tipo di oggetto TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="ae6d5-103">The TrustedDomain Object Type</span></span>

<span data-ttu-id="ae6d5-104">I sistemi basati su Windows possono avere più istanze del tipo di oggetto [**trustedDomain**](trusteddomain-object.md) .</span><span class="sxs-lookup"><span data-stu-id="ae6d5-104">Windows-based systems can have multiple instances of the [**TrustedDomain**](trusteddomain-object.md) object type.</span></span> <span data-ttu-id="ae6d5-105">Gli oggetti **trustedDomain** hanno due campi che devono essere univoci tra tutti gli oggetti **trustedDomain** :</span><span class="sxs-lookup"><span data-stu-id="ae6d5-105">**TrustedDomain** objects have two fields that must be unique among all **TrustedDomain** objects:</span></span>

-   <span data-ttu-id="ae6d5-106">Nome del [ **trustedDomain**](trusteddomain-object.md)</span><span class="sxs-lookup"><span data-stu-id="ae6d5-106">The name of the [**TrustedDomain**](trusteddomain-object.md)</span></span>
-   <span data-ttu-id="ae6d5-107">[*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) di [**trustedDomain**](trusteddomain-object.md).</span><span class="sxs-lookup"><span data-stu-id="ae6d5-107">The [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the [**TrustedDomain**](trusteddomain-object.md).</span></span>

<span data-ttu-id="ae6d5-108">Il tentativo di creare un nuovo oggetto **trustedDomain** con un nome o un SID già in uso da un altro oggetto **trustedDomain** verrà rifiutato.</span><span class="sxs-lookup"><span data-stu-id="ae6d5-108">An attempt to create a new **TrustedDomain** object with either a name or SID that is already in use by another **TrustedDomain** object will be rejected.</span></span>

 

 
