---
description: Aggiungere tutte le proprietà della password dalla tabella CustomUserAccounts alla proprietà MsiHiddenProperties nella tabella delle proprietà.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Sicurezza dell'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968672"
---
# <a name="securing-the-installation"></a><span data-ttu-id="c841c-103">Sicurezza dell'installazione</span><span class="sxs-lookup"><span data-stu-id="c841c-103">Securing the Installation</span></span>

<span data-ttu-id="c841c-104">Aggiungere tutte le proprietà della password dalla tabella CustomUserAccounts alla proprietà [**MsiHiddenProperties**](msihiddenproperties.md) nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="c841c-104">Add all of the Password properties from the CustomUserAccounts table to the [**MsiHiddenProperties**](msihiddenproperties.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="c841c-105">Aggiungere anche i nomi delle azioni personalizzate posticipate alla proprietà **MsiHiddenProperties** .</span><span class="sxs-lookup"><span data-stu-id="c841c-105">Add the names of the deferred custom actions to the **MsiHiddenProperties** property as well.</span></span> <span data-ttu-id="c841c-106">Ciò impedirà al programma di installazione di scrivere i valori delle proprietà sensibili (le password) nel log e garantirà che questi valori non vengano registrati quando le azioni personalizzate posticipate utilizzano i valori come proprietà CustomActionData.</span><span class="sxs-lookup"><span data-stu-id="c841c-106">This will prevent the installer from writing the sensitive property values (the passwords) into the log and will ensure these values are not logged when the deferred custom actions use the values as the CustomActionData property.</span></span>

<span data-ttu-id="c841c-107">Affinché la password dell'utente sia disponibile nel servizio Windows Installer, è necessario aggiungere la proprietà password alla proprietà [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="c841c-107">For the user's password to be available in the Windows Installer service, the password property must be added to the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

[<span data-ttu-id="c841c-108">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="c841c-108">Property Table</span></span>](property-table.md)



| <span data-ttu-id="c841c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c841c-109">Property</span></span>                                                 | <span data-ttu-id="c841c-110">Valore</span><span class="sxs-lookup"><span data-stu-id="c841c-110">Value</span></span>                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="c841c-111">**MsiHiddenProperties**</span><span class="sxs-lookup"><span data-stu-id="c841c-111">**MsiHiddenProperties**</span></span>](msihiddenproperties.md)       | <span data-ttu-id="c841c-112">TESTUSERPASSWORD; CreateAccount RemoveAccount RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="c841c-112">TESTUSERPASSWORD;CreateAccount;RemoveAccount;RollbackAccount</span></span> |
| [<span data-ttu-id="c841c-113">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="c841c-113">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="c841c-114">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="c841c-114">TESTUSERPASSWORD</span></span>                                             |



 

<span data-ttu-id="c841c-115">Si conclude l'esempio.</span><span class="sxs-lookup"><span data-stu-id="c841c-115">This concludes the sample.</span></span>

 

 



