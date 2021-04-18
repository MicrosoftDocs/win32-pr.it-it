---
description: La tabella ModuleSignature contiene tutte le informazioni necessarie per identificare il modulo merge.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Creazione di tabelle ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796775b0237c17db4fa21075a792c372bed3e97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311038"
---
# <a name="authoring-modulesignature-tables"></a><span data-ttu-id="9cb3a-103">Creazione di tabelle ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="9cb3a-103">Authoring ModuleSignature Tables</span></span>

<span data-ttu-id="9cb3a-104">La [tabella ModuleSignature](modulesignature-table.md) contiene tutte le informazioni necessarie per identificare il modulo merge.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-104">The [ModuleSignature table](modulesignature-table.md) contains all the information needed to identify the merge module.</span></span>

<span data-ttu-id="9cb3a-105">Il campo ModuleID è la chiave primaria per questa tabella e deve seguire la convenzione descritta in [denominazione delle chiavi primarie nei database dei moduli di Unione](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="9cb3a-105">The ModuleID field is the primary key for this table and must follow the convention described in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span> <span data-ttu-id="9cb3a-106">Se, ad esempio, il nome leggibile del modulo merge è MyLibrary e il GUID del modulo merge è {880DE2F0-CDD8-11D1-A849-006097ABDE17}, la voce nella colonna ModuleID della tabella ModuleSignature diventa MyLibrary. 880DE2F0 CDD8 11D1 A849 006097ABDE17 \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9cb3a-106">For example, if the readable name of the merge module is MyLibrary and the GUID for the merge module is {880DE2F0-CDD8-11D1-A849-006097ABDE17}, the entry in the ModuleID column of the ModuleSignature table becomes MyLibrary.880DE2F0\_CDD8\_11D1\_A849\_006097ABDE17.</span></span>

<span data-ttu-id="9cb3a-107">Immettere l'identificatore decimale per la lingua predefinita del modulo merge nel campo Language della tabella ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-107">Enter the decimal identifier for the default language of the merge module into the Language field of the ModuleSignature table.</span></span>

<span data-ttu-id="9cb3a-108">Immettere la versione del modulo merge nel campo versione.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-108">Enter the version of the merge module into the Version field.</span></span>

 

 



