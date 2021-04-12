---
description: Prima che il sottosistema smart card possa trovare una smart card, la smart card deve essere introdotta nel sistema.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Introduzione di smart card al sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233270"
---
# <a name="introducing-smart-cards-to-the-system"></a><span data-ttu-id="cd690-103">Introduzione di smart card al sistema</span><span class="sxs-lookup"><span data-stu-id="cd690-103">Introducing Smart Cards to the System</span></span>

<span data-ttu-id="cd690-104">Prima che il [*sottosistema Smart Card*](../secgloss/s-gly.md) possa trovare una [*Smart Card*](../secgloss/s-gly.md), la smart card deve essere introdotta nel sistema.</span><span class="sxs-lookup"><span data-stu-id="cd690-104">Before the [*smart card subsystem*](../secgloss/s-gly.md) can find a [*smart card*](../secgloss/s-gly.md), the smart card must be introduced to the system.</span></span> <span data-ttu-id="cd690-105">Questa operazione viene in genere eseguita con uno strumento di configurazione della smart card fornito dal produttore della scheda.</span><span class="sxs-lookup"><span data-stu-id="cd690-105">This is typically done with a smart card setup tool provided by the card manufacturer.</span></span> <span data-ttu-id="cd690-106">Lo strumento può essere un programma su un disco floppy (con la smart card), un controllo ActiveX disponibile in un sito Web e così via.</span><span class="sxs-lookup"><span data-stu-id="cd690-106">The tool could come as a program on a floppy disk (with the smart card), an ActiveX control available on a website, and so on.</span></span>

<span data-ttu-id="cd690-107">Lo strumento di installazione di deve fornire le seguenti informazioni sulla scheda:</span><span class="sxs-lookup"><span data-stu-id="cd690-107">The setup tool must provide the following pieces of information about the card:</span></span>

-   <span data-ttu-id="cd690-108">La relativa [*stringa ATR*](../secgloss/a-gly.md)e una maschera facoltativa da usare come supporto per l'identificazione della scheda.</span><span class="sxs-lookup"><span data-stu-id="cd690-108">Its [*ATR string*](../secgloss/a-gly.md), and an optional mask to use as an aid in identifying the card.</span></span>
-   <span data-ttu-id="cd690-109">Elenco di interfacce di smart card supportate dalla scheda.</span><span class="sxs-lookup"><span data-stu-id="cd690-109">A list of smart card interfaces supported by the card.</span></span>
-   <span data-ttu-id="cd690-110">Nome visualizzato per la scheda da utilizzare per l'identificazione della scheda per l'utente.</span><span class="sxs-lookup"><span data-stu-id="cd690-110">A display name for the card, to be used in identifying the card to the user.</span></span> <span data-ttu-id="cd690-111">Nella maggior parte dei casi, l'utente lo fornirà allo strumento di configurazione di.</span><span class="sxs-lookup"><span data-stu-id="cd690-111">In most cases, the user will supply this to the setup tool.</span></span>
-   <span data-ttu-id="cd690-112">[*Provider di servizi primario*](../secgloss/p-gly.md) associato alla scheda (facoltativo), da utilizzare per l'accesso alla scheda tramite interfacce com.</span><span class="sxs-lookup"><span data-stu-id="cd690-112">The [*primary service provider*](../secgloss/p-gly.md) associated with the card (optional), to be used when accessing the card through COM interfaces.</span></span>

<span data-ttu-id="cd690-113">Per semplificare gli strumenti di configurazione e per garantire l'integrità del [*database delle smart card*](../secgloss/s-gly.md), il sottosistema smart card fornisce le due funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="cd690-113">To simplify setup tools, and to ensure the integrity of the [*smart card database*](../secgloss/s-gly.md), the smart card subsystem provides the following two functions.</span></span> <span data-ttu-id="cd690-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduce una smart card nel database e [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) la rimuove dal database.</span><span class="sxs-lookup"><span data-stu-id="cd690-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduces a smart card into the database and [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) removes it from the database.</span></span>

 

 
