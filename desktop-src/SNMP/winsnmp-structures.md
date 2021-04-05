---
title: Strutture WinSNMP
description: Le funzioni API WinSNMP utilizzano le strutture seguenti.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- WinSNMP strutture SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872717"
---
# <a name="winsnmp-structures"></a><span data-ttu-id="e23df-104">Strutture WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e23df-104">WinSNMP Structures</span></span>

<span data-ttu-id="e23df-105">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="e23df-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e23df-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e23df-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e23df-107">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="e23df-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="e23df-108">Le funzioni API WinSNMP utilizzano le strutture seguenti.</span><span class="sxs-lookup"><span data-stu-id="e23df-108">The WinSNMP API functions use the following structures.</span></span>



| <span data-ttu-id="e23df-109">Struttura</span><span class="sxs-lookup"><span data-stu-id="e23df-109">Structure</span></span>                                  | <span data-ttu-id="e23df-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e23df-110">Description</span></span>                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e23df-111">**smiCNTR64**</span><span class="sxs-lookup"><span data-stu-id="e23df-111">**smiCNTR64**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | <span data-ttu-id="e23df-112">Contiene un valore Unsigned Integer a 64 bit che rappresenta un contatore.</span><span class="sxs-lookup"><span data-stu-id="e23df-112">Contains a 64-bit unsigned integer value that represents a counter.</span></span>                                                    |
| [<span data-ttu-id="e23df-113">**smiOCTETS**</span><span class="sxs-lookup"><span data-stu-id="e23df-113">**smiOCTETS**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | <span data-ttu-id="e23df-114">Contiene un puntatore a una stringa di ottetto SNMP di lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="e23df-114">Contains a pointer to an SNMP octet string of variable length.</span></span>                                                         |
| [<span data-ttu-id="e23df-115">**smiOID**</span><span class="sxs-lookup"><span data-stu-id="e23df-115">**smiOID**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | <span data-ttu-id="e23df-116">Contiene un puntatore a una matrice di lunghezza variabile dei sottoidentificatori associati a un oggetto denominato specificato.</span><span class="sxs-lookup"><span data-stu-id="e23df-116">Contains a pointer to a variable length array of the subidentifiers that are associated with a specified named object.</span></span> |
| [<span data-ttu-id="e23df-117">**smiVALUE**</span><span class="sxs-lookup"><span data-stu-id="e23df-117">**smiVALUE**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | <span data-ttu-id="e23df-118">Rappresenta il valore associato a un nome di variabile in una voce di associazione variabile.</span><span class="sxs-lookup"><span data-stu-id="e23df-118">Represents the value that is associated with a variable name in a variable binding entry.</span></span>                              |
| [<span data-ttu-id="e23df-119">**smiVENDORINFO**</span><span class="sxs-lookup"><span data-stu-id="e23df-119">**smiVENDORINFO**</span></span>](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | <span data-ttu-id="e23df-120">Contiene informazioni sull'implementazione Microsoft di WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="e23df-120">Contains information about the Microsoft implementation of WinSNMP.</span></span>                                                    |



 

 

 