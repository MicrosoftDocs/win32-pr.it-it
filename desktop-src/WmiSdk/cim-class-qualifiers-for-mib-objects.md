---
description: Il provider SNMP usa i qualificatori di classe CIM seguenti per eseguire il mapping delle definizioni di oggetti MIB alle definizioni di classi CIM.
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: Qualificatori di classe CIM per oggetti MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233251"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a><span data-ttu-id="fab84-103">Qualificatori di classe CIM per oggetti MIB</span><span class="sxs-lookup"><span data-stu-id="fab84-103">CIM Class Qualifiers for MIB Objects</span></span>

<span data-ttu-id="fab84-104">Il provider SNMP usa i qualificatori di classe CIM seguenti per eseguire il mapping delle definizioni di oggetti MIB alle definizioni di classi CIM.</span><span class="sxs-lookup"><span data-stu-id="fab84-104">The SNMP Provider uses the following CIM class qualifiers when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="fab84-105">Per il provider SNMP per la risoluzione completa di un oggetto gruppo, è necessario che sia presente un qualificatore obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fab84-105">A mandatory qualifier must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="fab84-106">La mancata definizione di un qualificatore obbligatorio restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="fab84-106">Failure to define a mandatory qualifier returns an error.</span></span> <span data-ttu-id="fab84-107">Se si specifica un valore qualificatore non valido, viene restituito anche un errore.</span><span class="sxs-lookup"><span data-stu-id="fab84-107">Specifying an illegal qualifier value also returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="fab84-108">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fab84-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 



| <span data-ttu-id="fab84-109">Qualifier</span><span class="sxs-lookup"><span data-stu-id="fab84-109">Qualifier</span></span>           | <span data-ttu-id="fab84-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fab84-110">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fab84-111">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="fab84-111">**Description**</span></span>     | <span data-ttu-id="fab84-112">**stringa** di Opzionale</span><span class="sxs-lookup"><span data-stu-id="fab84-112">**string** Optional</span></span><br/> <span data-ttu-id="fab84-113">Descrizione della classe.</span><span class="sxs-lookup"><span data-stu-id="fab84-113">Description of the class.</span></span><br/>                                                                      |
| <span data-ttu-id="fab84-114">**ObjectId del gruppo \_**</span><span class="sxs-lookup"><span data-stu-id="fab84-114">**Group\_Objectid**</span></span> | <span data-ttu-id="fab84-115">**stringa** di Obbligatoria, se la classe è per il provider di classi SNMP.</span><span class="sxs-lookup"><span data-stu-id="fab84-115">**string** Mandatory, if the class is for the SNMP class provider.</span></span><br/> <span data-ttu-id="fab84-116">Identificatore di oggetto della raccolta fabbricata.</span><span class="sxs-lookup"><span data-stu-id="fab84-116">Object identifier of the fabricated collection.</span></span><br/> |
| <span data-ttu-id="fab84-117">**Importazioni di moduli \_**</span><span class="sxs-lookup"><span data-stu-id="fab84-117">**Module\_Imports**</span></span> | <span data-ttu-id="fab84-118">**stringa** di Opzionale</span><span class="sxs-lookup"><span data-stu-id="fab84-118">**string** Optional</span></span><br/> <span data-ttu-id="fab84-119">Elenco delimitato da virgole di nomi di moduli MIB usati per risolvere le importazioni.</span><span class="sxs-lookup"><span data-stu-id="fab84-119">Comma-separated list of MIB module names used to resolve imports.</span></span><br/>                              |
| <span data-ttu-id="fab84-120">**Nome del modulo \_**</span><span class="sxs-lookup"><span data-stu-id="fab84-120">**Module\_Name**</span></span>    | <span data-ttu-id="fab84-121">**stringa** di Opzionale</span><span class="sxs-lookup"><span data-stu-id="fab84-121">**string** Optional</span></span><br/> <span data-ttu-id="fab84-122">Nome identità di un modulo MIB.</span><span class="sxs-lookup"><span data-stu-id="fab84-122">Identity name of a MIB module.</span></span><br/>                                                                 |
| <span data-ttu-id="fab84-123">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fab84-123">**Reference**</span></span>       | <span data-ttu-id="fab84-124">**stringa** di Opzionale</span><span class="sxs-lookup"><span data-stu-id="fab84-124">**string** Optional</span></span><br/> <span data-ttu-id="fab84-125">Fa riferimento a un altro documento che contiene ulteriori informazioni sulla classe.</span><span class="sxs-lookup"><span data-stu-id="fab84-125">Refers to another document that contains more information about the class.</span></span><br/>                     |
| <span data-ttu-id="fab84-126">**Singleton**</span><span class="sxs-lookup"><span data-stu-id="fab84-126">**Singleton**</span></span>       | <span data-ttu-id="fab84-127">**Bool** Obbligatorio per le classi mappate da raccolte scalari.</span><span class="sxs-lookup"><span data-stu-id="fab84-127">**Bool** Mandatory for classes mapped from scalar collections.</span></span><br/> <span data-ttu-id="fab84-128">Indica una classe che può avere una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="fab84-128">Indicates a class that can only have one instance.</span></span><br/>  |



 

 

 




