---
description: La sintassi dei messaggi crittografici (CMS), derivata da PKCS \# 7 versione 1,5, è la sintassi usata per eseguire l'hashing, firmare digitalmente, autenticare e crittografare i messaggi arbitrari.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: Aggiunte CMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309983"
---
# <a name="cms-additions"></a><span data-ttu-id="e69d8-103">Aggiunte CMS</span><span class="sxs-lookup"><span data-stu-id="e69d8-103">CMS Additions</span></span>

<span data-ttu-id="e69d8-104">La sintassi dei messaggi crittografici (CMS), derivata da PKCS \# 7 versione 1,5, è la sintassi usata per eseguire l' [*hashing*](../secgloss/h-gly.md), [*firmare digitalmente*](../secgloss/d-gly.md), autenticare e crittografare i messaggi arbitrari.</span><span class="sxs-lookup"><span data-stu-id="e69d8-104">Cryptographic Message Syntax (CMS), derived from PKCS \#7 version 1.5, is the syntax used to [*hash*](../secgloss/h-gly.md), [*digitally sign*](../secgloss/d-gly.md), authenticate, and encrypt arbitrary messages.</span></span> <span data-ttu-id="e69d8-105">Laddove possibile, viene mantenuta la compatibilità con le versioni precedenti; sono state tuttavia apportate modifiche per supportare il trasferimento di certificati degli attributi e le tecniche di accordo chiave per la gestione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="e69d8-105">Where possible, backward compatibility is preserved; however, changes have been made to accommodate attribute certificate transfer and key agreement techniques for key management.</span></span> <span data-ttu-id="e69d8-106">CMS consente più incapsulamento in modo che una busta di incapsulamento possa essere annidata all'interno di un'altra.</span><span class="sxs-lookup"><span data-stu-id="e69d8-106">CMS allows multiple encapsulation so that one encapsulation envelope can be nested inside another.</span></span> <span data-ttu-id="e69d8-107">Inoltre, un'entità può firmare digitalmente i dati incapsulati in precedenza; gli attributi arbitrari, ad esempio l'ora di firma, possono essere firmati insieme al contenuto del messaggio. gli attributi e, ad esempio [*controfirme*](../secgloss/c-gly.md), possono essere associati a una firma.</span><span class="sxs-lookup"><span data-stu-id="e69d8-107">Also, one party can digitally sign previously encapsulated data; arbitrary attributes, such as signing time, can be signed along with the message content; and attributes, such as [*countersignatures*](../secgloss/c-gly.md), can be associated with a signature.</span></span> <span data-ttu-id="e69d8-108">CMS può supportare un'ampia gamma di architetture per la gestione delle chiavi basata sui certificati.</span><span class="sxs-lookup"><span data-stu-id="e69d8-108">CMS can support a variety of architectures for certificate-based key management.</span></span>

<span data-ttu-id="e69d8-109">Per supportare altre funzionalità di CMS, alle strutture di dati sottostanti sono stati assegnati nuovi campi.</span><span class="sxs-lookup"><span data-stu-id="e69d8-109">To support additional CMS capabilities, underlying data structures have been given new fields.</span></span> <span data-ttu-id="e69d8-110">Sono stati aggiunti anche nuovi flag e valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="e69d8-110">New flags and parameter values have also been added.</span></span> <span data-ttu-id="e69d8-111">Tutte le strutture di dati e tutte le API che usano CMS sono compatibili con le versioni precedenti del 100% con PKCS \# 7 versione 1,5.</span><span class="sxs-lookup"><span data-stu-id="e69d8-111">All data structures and all APIs using CMS are 100 percent backward compatible with PKCS \#7 version 1.5.</span></span>

<span data-ttu-id="e69d8-112">Sono incluse aggiunte di [dati in busta](enveloped-data-additions.md) e aggiunte di [dati firmati](signed-data-additions.md).</span><span class="sxs-lookup"><span data-stu-id="e69d8-112">Additions include [Enveloped Data Additions](enveloped-data-additions.md) and [Signed Data Additions](signed-data-additions.md).</span></span>

 

 
