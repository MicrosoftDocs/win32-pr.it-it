---
title: Panoramica dell'architettura SSPI
description: SSPI è un'interfaccia software.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047090"
---
# <a name="sspi-architectural-overview"></a><span data-ttu-id="96b55-103">Panoramica dell'architettura SSPI</span><span class="sxs-lookup"><span data-stu-id="96b55-103">SSPI Architectural Overview</span></span>

<span data-ttu-id="96b55-104">SSPI è un'interfaccia software.</span><span class="sxs-lookup"><span data-stu-id="96b55-104">SSPI is a software interface.</span></span> <span data-ttu-id="96b55-105">Le librerie di programmazione distribuite, ad esempio RPC, possono usarle per le comunicazioni autenticate.</span><span class="sxs-lookup"><span data-stu-id="96b55-105">Distributed programming libraries such as RPC can use it for authenticated communications.</span></span> <span data-ttu-id="96b55-106">Uno o più moduli software forniscono le effettive funzionalità di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="96b55-106">One or more software modules provide the actual authentication capabilities.</span></span> <span data-ttu-id="96b55-107">Ogni modulo, denominato SSP (Security Support Provider), viene implementato come libreria a collegamento dinamico (DLL).</span><span class="sxs-lookup"><span data-stu-id="96b55-107">Each module, called a security support provider (SSP), is implemented as a dynamic link library (DLL).</span></span> <span data-ttu-id="96b55-108">Un SSP fornisce uno o più pacchetti di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="96b55-108">An SSP provides one or more security packages.</span></span>

<span data-ttu-id="96b55-109">Sono disponibili diversi SSP e pacchetti.</span><span class="sxs-lookup"><span data-stu-id="96b55-109">A variety of SSPs and packages are available.</span></span> <span data-ttu-id="96b55-110">Windows viene fornito con il pacchetto di sicurezza NTLM e il pacchetto di sicurezza del protocollo Kerberos di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96b55-110">Windows ships with the NTLM security package and the Microsoft Kerberos protocol security package.</span></span> <span data-ttu-id="96b55-111">Inoltre, è possibile scegliere di installare il pacchetto di sicurezza SSL (Secure Socket Layer) o qualsiasi altro SSP compatibile con SSPI.</span><span class="sxs-lookup"><span data-stu-id="96b55-111">In addition, you may choose to install the Secure Socket Layer (SSL) security package, or any other SSPI-compatible SSP.</span></span>

<span data-ttu-id="96b55-112">L'uso di SSPI garantisce che, indipendentemente dall'SSP selezionato, l'applicazione acceda alle funzionalità di autenticazione in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="96b55-112">Using SSPI ensures that no matter which SSP you select, your application accesses the authentication features in a uniform manner.</span></span> <span data-ttu-id="96b55-113">Questa funzionalità consente all'applicazione di ottenere una maggiore indipendenza dall'implementazione della rete rispetto a quella disponibile in passato.</span><span class="sxs-lookup"><span data-stu-id="96b55-113">This capability provides your application greater independence from the implementation of the network than was available in the past.</span></span>

<span data-ttu-id="96b55-114">Le applicazioni distribuite comunicano tramite l'interfaccia RPC.</span><span class="sxs-lookup"><span data-stu-id="96b55-114">Distributed applications communicate through the RPC interface.</span></span> <span data-ttu-id="96b55-115">Il software RPC a sua volta accede alle funzionalità di autenticazione di un provider di servizi condivisi tramite SSPI.</span><span class="sxs-lookup"><span data-stu-id="96b55-115">The RPC software in turn, accesses the authentication features of an SSP through the SSPI.</span></span>

<span data-ttu-id="96b55-116">Per ulteriori informazioni, vedere [SSPI](/windows/desktop/SecAuthN/sspi).</span><span class="sxs-lookup"><span data-stu-id="96b55-116">For more information, see [SSPI](/windows/desktop/SecAuthN/sspi).</span></span>

 

 