---
title: Accesso a Active Directory tramite Visual Basic
description: Una delle funzionalità più potenti rese disponibili con il sistema operativo Microsoft Windows 2000 è il servizio directory Microsoft Active Directory.
ms.assetid: b5021e38-92a2-43d2-b3cb-15ff5c74c1d8
ms.tgt_platform: multiple
keywords:
- Accesso a Active Directory tramite Visual Basic ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbc469de112c37c1c2ea5865d88252c4bd98466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044083"
---
# <a name="accessing-active-directory-using-visual-basic"></a><span data-ttu-id="8e5f2-104">Accesso a Active Directory tramite Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8e5f2-104">Accessing Active Directory Using Visual Basic</span></span>

<span data-ttu-id="8e5f2-105">Una delle funzionalità più potenti rese disponibili con il sistema operativo Microsoft Windows 2000 è il servizio directory Microsoft Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-105">One of the most powerful features that became available with the Microsoft Windows 2000 operating system is the Microsoft Active Directory directory service.</span></span> <span data-ttu-id="8e5f2-106">Quando si accede a un dominio Windows 2000, Active Directory viene attivato. per cercare la stampante di colori più vicina nella compilazione, è possibile usare Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-106">When you log on to a Windows 2000 domain, Active Directory is put into action; to search for the closest color printer in your building, you can use Active Directory.</span></span> <span data-ttu-id="8e5f2-107">Può essere usato per la ricerca di una rubrica o per cercare gli utenti che lavorano nell'edificio 40.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-107">It can be used for an address book lookup or a search for users who work in building 40.</span></span> <span data-ttu-id="8e5f2-108">Con Active Directory, è possibile usare una smart card per accedere a un dominio di Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-108">With Active Directory, you can use a smart card to log on to a Windows 2000 domain.</span></span> <span data-ttu-id="8e5f2-109">È anche possibile unire i dati del software Microsoft SQL Server database e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-109">You can even join data from Microsoft SQL Server database software and Active Directory.</span></span>

<span data-ttu-id="8e5f2-110">Molte altre tecnologie Microsoft, ad esempio Microsoft Message Queue Server (MSMQ), COM (archivio classi), Internet Protocol Security (IPsec), oggetti Criteri di gruppo (GPO) ed Exchange sono integrate con Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-110">Many other Microsoft technologies, such as Microsoft Message Queue Server (MSMQ), COM (Class Store), Internet Protocol security (IPsec), Group Policy Objects (GPOs), and Exchange are integrated with Active Directory.</span></span>

<span data-ttu-id="8e5f2-111">In questa sezione viene illustrato come utilizzare ADSI (Active Directory Service Interfaces) per accedere a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-111">This section discusses how to use the Active Directory Service Interfaces (ADSI) to access Active Directory.</span></span> <span data-ttu-id="8e5f2-112">Utilizzando uno scenario per una società fittizia (Fabrikam Corporation), si apprenderà come eseguire alcune attività amministrative di base.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-112">Using a scenario for a fictitious company — the Fabrikam Corporation — you will learn how to perform some basic administrative tasks.</span></span>

<span data-ttu-id="8e5f2-113">Quando si procede in questo scenario, gli esempi di codice in ogni sezione si basano su se stessi.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-113">As you progress through this scenario, the code examples in each section build upon themselves.</span></span>

<span data-ttu-id="8e5f2-114">Per brevità, tutti gli esempi di codice sono scritti con il sistema di sviluppo Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-114">For brevity, all code examples are written with the Microsoft Visual Basic development system.</span></span> <span data-ttu-id="8e5f2-115">Per ulteriori informazioni sulla conversione C++, vedere [mapping di codice ADSI Visual Basic al codice c++](mapping-adsi-visual-basic-code-to-c-code.md).</span><span class="sxs-lookup"><span data-stu-id="8e5f2-115">For more information about C++ conversion, see [Mapping ADSI Visual Basic Code to C++ Code](mapping-adsi-visual-basic-code-to-c-code.md).</span></span>

 

 




