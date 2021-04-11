---
description: Una sessione di accesso è una sessione di elaborazione che inizia quando l'autenticazione utente ha esito positivo e termina quando l'utente si disconnette dal sistema.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: Sessioni di accesso LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32a4912218b68c25c5c23334f7b34ef875fa318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232833"
---
# <a name="lsa-logon-sessions"></a><span data-ttu-id="cfb65-103">Sessioni di accesso LSA</span><span class="sxs-lookup"><span data-stu-id="cfb65-103">LSA Logon Sessions</span></span>

<span data-ttu-id="cfb65-104">Una [*sessione di accesso*](../secgloss/l-gly.md) è una sessione di elaborazione che inizia quando l'autenticazione utente ha esito positivo e termina quando l'utente si disconnette dal sistema.</span><span class="sxs-lookup"><span data-stu-id="cfb65-104">A [*logon session*](../secgloss/l-gly.md) is a computing session that begins when a user authentication is successful and ends when the user logs off of the system.</span></span>

<span data-ttu-id="cfb65-105">Quando un utente viene autenticato correttamente, il pacchetto di autenticazione crea una sessione di accesso e restituisce informazioni all' [*autorità di sicurezza locale*](../secgloss/l-gly.md) (LSA) utilizzata per creare un [*token*](../secgloss/t-gly.md) per il nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="cfb65-105">When a user is successfully authenticated, the authentication package creates a logon session and returns information to the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) that is used to create a [*token*](../secgloss/t-gly.md) for the new user.</span></span> <span data-ttu-id="cfb65-106">Questo token include, tra le altre cose, un [*identificatore univoco locale*](../secgloss/l-gly.md) (LUID) per la sessione di accesso, denominato [*ID di accesso*](../secgloss/l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cfb65-106">This token includes, among other things, a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) for the logon session, called the [*logon Id*](../secgloss/l-gly.md).</span></span>

<span data-ttu-id="cfb65-107">Quando viene creato un token, il [*conteggio dei riferimenti*](../secgloss/r-gly.md) per la sessione di accesso viene incrementato.</span><span class="sxs-lookup"><span data-stu-id="cfb65-107">When a token is created, the [*reference count*](../secgloss/r-gly.md) for the logon session is incremented.</span></span> <span data-ttu-id="cfb65-108">Il conteggio dei riferimenti viene incrementato anche ogni volta che vengono create copie del token per la creazione, la rappresentazione o altri usi del processo.</span><span class="sxs-lookup"><span data-stu-id="cfb65-108">The reference count is also incremented whenever copies of the token are created for process creation, impersonation, or other uses.</span></span> <span data-ttu-id="cfb65-109">Quando vengono completati i token utilizzati e le copie del token vengono eliminate, il conteggio dei riferimenti per la sessione di accesso viene decrementato.</span><span class="sxs-lookup"><span data-stu-id="cfb65-109">As token uses are completed and copies of the token are deleted, the reference count for the logon session is decremented.</span></span> <span data-ttu-id="cfb65-110">Quando il conteggio dei riferimenti raggiunge zero, la sessione di accesso viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="cfb65-110">When the reference count reaches zero, the logon session is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="cfb65-111">Se l'autenticazione ha esito negativo, il [*pacchetto di autenticazione*](../secgloss/a-gly.md) non deve creare una sessione di accesso.</span><span class="sxs-lookup"><span data-stu-id="cfb65-111">If authentication is not successful, the [*authentication package*](../secgloss/a-gly.md) should not create a logon session.</span></span> <span data-ttu-id="cfb65-112">Se il pacchetto di autenticazione deve creare una sessione di accesso prima di prendere una decisione finale sulla validità dell'utente e se l'autenticazione ha esito negativo, il pacchetto di autenticazione deve eliminare la sessione.</span><span class="sxs-lookup"><span data-stu-id="cfb65-112">If the authentication package must create a logon session before making a final determination about the validity of the user, and if authentication fails, the authentication package must delete the session.</span></span>

 

 

 
