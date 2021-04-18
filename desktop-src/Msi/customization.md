---
description: Poiché il Windows Installer conserva tutte le informazioni sull'installazione di in un database relazionale, l'installazione di un'applicazione o di un prodotto può essere personalizzata per gruppi di utenti specifici applicando operazioni di trasformazione al pacchetto.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307844"
---
# <a name="customization"></a><span data-ttu-id="80972-103">Personalizzazione</span><span class="sxs-lookup"><span data-stu-id="80972-103">Customization</span></span>

<span data-ttu-id="80972-104">Poiché il Windows Installer conserva tutte le informazioni sull'installazione di in un database relazionale, l'installazione di un'applicazione o di un prodotto può essere personalizzata per gruppi di utenti specifici applicando operazioni di trasformazione al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="80972-104">Because the Windows Installer keeps all information about the installation in a relational database, the installation of an application or product can be customized for particular user groups by applying transform operations to the package.</span></span> <span data-ttu-id="80972-105">Le trasformazioni possono essere utilizzate per incapsulare le varie personalizzazioni di un pacchetto di base richiesto da gruppi di lavoro diversi.</span><span class="sxs-lookup"><span data-stu-id="80972-105">Transforms can be used to encapsulate the various customizations of a base package required by different workgroups.</span></span> <span data-ttu-id="80972-106">Per altre informazioni, vedere [unioni e trasformazioni](merges-and-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="80972-106">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

<span data-ttu-id="80972-107">Durante l'installazione è possibile applicare più trasformazioni di un pacchetto di base in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="80972-107">Multiple transforms of a base package can be applied on-the-fly during installation.</span></span> <span data-ttu-id="80972-108">Questo fornisce un meccanismo per assegnare in modo efficiente installazioni personalizzate a diversi gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="80972-108">This provides a mechanism for efficiently assigning customized installations to different groups of users.</span></span> <span data-ttu-id="80972-109">Questo, ad esempio, può essere utile nelle organizzazioni in cui i reparti di supporto per Finanza e personale richiedono installazioni diverse di un determinato prodotto.</span><span class="sxs-lookup"><span data-stu-id="80972-109">For example, this would be useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="80972-110">Il prodotto può essere reso disponibile a tutti gli utenti dell'organizzazione mediante un' [installazione amministrativa](administrative-installation.md) del pacchetto di base in un singolo punto di installazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="80972-110">The product can be made available to everyone in the organization by an [administrative installation](administrative-installation.md) of the base package to a single administrative installation point.</span></span> <span data-ttu-id="80972-111">Ogni gruppo di lavoro può quindi ricevere automaticamente la personalizzazione appropriata per mezzo di una trasformazione immediata al momento dell'installazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="80972-111">Each work group can then automatically receive their appropriate customization by means of an on-the-fly transform when they install the product.</span></span>

 

 



