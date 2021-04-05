---
description: Quando ci si connette in remoto a un server Active Directory diverso da quello del dominio corrente, è necessario specificare il nome di un computer che è già membro del dominio appartenente al Active Directory desiderato.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Descrizione dello spazio dei nomi LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1f27c3e2ebc48a0dfa14563822e34bc06d6223
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058018"
---
# <a name="describing-the-ldap-namespace"></a><span data-ttu-id="4d09d-103">Descrizione dello spazio dei nomi LDAP</span><span class="sxs-lookup"><span data-stu-id="4d09d-103">Describing the LDAP Namespace</span></span>

<span data-ttu-id="4d09d-104">Quando ci si connette in remoto a un server Active Directory diverso da quello del dominio corrente, è necessario specificare il nome di un computer che è già membro del dominio appartenente al Active Directory desiderato.</span><span class="sxs-lookup"><span data-stu-id="4d09d-104">When connecting remotely to an Active Directory server other than the one in your current domain, you must specify the name of a computer that is already a member of the domain belonging to the Active Directory you want.</span></span>

<span data-ttu-id="4d09d-105">Per connettersi in remoto a un computer che è già membro del dominio appartenente al server Active Directory, digitare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="4d09d-105">To remotely connect to a computer that is already a member of the domain belonging to the Active Directory server, type the following command.</span></span>

<span data-ttu-id="4d09d-106">**\\\\ComputerRemoto \\ \\ directory radice \\ LDAP**</span><span class="sxs-lookup"><span data-stu-id="4d09d-106">**\\\\RemoteComputer\\root\\directory\\LDAP**</span></span>

<span data-ttu-id="4d09d-107">Questo esempio mostra che sono presenti due parti che costituiscono un nome completo dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4d09d-107">This example shows that there are two parts that make up a fully qualified namespace name.</span></span> <span data-ttu-id="4d09d-108">La prima parte ( \\ \\ ComputerRemoto) rappresenta il computer che è già membro del dominio appartenente al server Active Directory desiderato.</span><span class="sxs-lookup"><span data-stu-id="4d09d-108">The first part (\\\\RemoteComputer) represents the computer that is already a member of the domain belonging to the Active Directory server you want.</span></span> <span data-ttu-id="4d09d-109">La seconda parte ( \\ \\ directory radice \\ LDAP) rappresenta lo schema Active Directory nel provider dei servizi directory.</span><span class="sxs-lookup"><span data-stu-id="4d09d-109">The second part (\\root\\directory\\LDAP) represents the Active Directory schema in the Directory Services Provider.</span></span>

> [!Note]  
> <span data-ttu-id="4d09d-110">Per ulteriori informazioni sul supporto e l'installazione di questo componente in un sistema operativo specifico, vedere la pagina relativa alla [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="4d09d-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



