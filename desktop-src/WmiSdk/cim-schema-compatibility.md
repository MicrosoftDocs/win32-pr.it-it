---
description: Compatibilità con lo schema CIM
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: Compatibilità con lo schema CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df559469ef6a8284b51951dc365bad6c302ca865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316572"
---
# <a name="cim-schema-compatibility"></a><span data-ttu-id="39182-103">Compatibilità con lo schema CIM</span><span class="sxs-lookup"><span data-stu-id="39182-103">CIM Schema Compatibility</span></span>

<span data-ttu-id="39182-104">Un componente chiave dell'infrastruttura di Strumentazione gestione Windows (WMI) è un modello orientato a oggetti delle entità gestibili in un sistema.</span><span class="sxs-lookup"><span data-stu-id="39182-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="39182-105">Il modello è conforme a uno standard gestito dal Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) ed è noto come Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="39182-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="39182-106">Lo schema CIM fornisce un unico meccanismo di descrizione dei dati per tutti i dati forniti.</span><span class="sxs-lookup"><span data-stu-id="39182-106">The CIM schema provides a single data description mechanism for any data that they provide.</span></span>

<span data-ttu-id="39182-107">A partire da Windows 7, WMI è compatibile con la versione dello schema CIM 2.17.1 ( [https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171) ).</span><span class="sxs-lookup"><span data-stu-id="39182-107">Starting in Windows 7, WMI is compatible with the CIM Schema version 2.17.1 ([https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171)).</span></span> <span data-ttu-id="39182-108">Gli utenti possono ora compilare uno schema definito da DMTF in un computer Windows.</span><span class="sxs-lookup"><span data-stu-id="39182-108">Users can now compile a DMTF defined schema on a Windows computer.</span></span>

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a><span data-ttu-id="39182-109">Vantaggi della compatibilità 2.17.1 della versione dello schema CIM</span><span class="sxs-lookup"><span data-stu-id="39182-109">Benefits of CIM Schema version 2.17.1 compatibility</span></span>

-   <span data-ttu-id="39182-110">Quando un utente Scarica file MOF 2.17.1 o DMTF MOF, questi ultimi possono essere compilati correttamente nel computer Windows di destinazione.</span><span class="sxs-lookup"><span data-stu-id="39182-110">When a user downloads CIM Schema version 2.17.1 or DMTF MOF files, they can be successfully compiled on the target Windows computer.</span></span>
-   <span data-ttu-id="39182-111">La versione dello schema CIM 2.17.1 ha aggiunto il supporto per BIOS, stampanti, messaggi standard, stato del sistema operativo, paradigmi di risparmio energia moderni, virtualizzazione e sicurezza.</span><span class="sxs-lookup"><span data-stu-id="39182-111">The CIM Schema version 2.17.1 added support for BIOS, printers, standard messages, operating system state, modern power management paradigms, virtualization and security.</span></span>
-   <span data-ttu-id="39182-112">La versione dello schema CIM 2.1.7.1 offre supporto del profilo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="39182-112">CIM Schema version 2.1.7.1 offers additional profile support.</span></span> <span data-ttu-id="39182-113">Per altre informazioni, vedere attraversamento di [associazioni tra spazi dei nomi](cross-namespace-association-traversal.md)</span><span class="sxs-lookup"><span data-stu-id="39182-113">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md)</span></span>

 

 



