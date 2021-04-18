---
title: Risparmio energia (servizi di base TPM)
description: TBS riceve gli eventi di risparmio energia.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "106299327"
---
# <a name="power-management-tpm-base-services"></a><span data-ttu-id="3a775-103">Risparmio energia (servizi di base TPM)</span><span class="sxs-lookup"><span data-stu-id="3a775-103">Power Management (TPM Base Services)</span></span>

<span data-ttu-id="3a775-104">TBS riceve gli eventi di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="3a775-104">The TBS receives power management events.</span></span> <span data-ttu-id="3a775-105">Quando viene ricevuta un'indicazione che il TPM o altre parti della piattaforma stanno per entrare in uno stato di alimentazione in cui l'esecuzione verrà interrotta o lo stato del TPM andrà perduto, TBS controlla per determinare se è probabile che il comando attualmente in esecuzione venga terminato prima che il sistema venga disattivato.</span><span class="sxs-lookup"><span data-stu-id="3a775-105">When an indication is received that the TPM or other parts of the platform are about to enter a power state in which execution will be interrupted or TPM state will be lost, the TBS checks to determine whether the currently executing command is likely to finish before the system powers down.</span></span> <span data-ttu-id="3a775-106">In generale, TBS consente il completamento dei comandi di durata breve e media, ma annulla i comandi a lunga durata.</span><span class="sxs-lookup"><span data-stu-id="3a775-106">In general, the TBS allows short and medium duration commands to finish, but cancels long duration commands.</span></span> <span data-ttu-id="3a775-107">Dopo che il comando ha restituito, TBS interrompe l'invio di nuovi comandi al TPM e si prepara per l'ibernazione.</span><span class="sxs-lookup"><span data-stu-id="3a775-107">After the command has returned, the TBS stops sending new commands to the TPM and prepares itself for hibernation.</span></span> <span data-ttu-id="3a775-108">Quando viene ripristinata l'alimentazione, TBS restituisce il risultato del comando al chiamante, quindi procede con l'elaborazione dei comandi TBS in sospeso.</span><span class="sxs-lookup"><span data-stu-id="3a775-108">When power is restored, the TBS returns the result of the command to the caller, and then proceeds with processing pending TBS commands.</span></span> <span data-ttu-id="3a775-109">Il codice di risparmio energia di TBS viene eseguito in modo asincrono, quindi può gestire le richieste di risparmio energia anche se il TPM sta elaborando un comando lungo.</span><span class="sxs-lookup"><span data-stu-id="3a775-109">The TBS power management code runs asynchronously, so it can handle power management requests even if the TPM is processing a long command.</span></span>

<span data-ttu-id="3a775-110">Quando un computer immette gli Stati di sospensione, inclusi S3 (sospensione) e S4 (ibernazione), il TPM è spento.</span><span class="sxs-lookup"><span data-stu-id="3a775-110">When a computer enters sleep states, including S3 (sleep) and S4 (hibernation), the TPM is powered off.</span></span> <span data-ttu-id="3a775-111">Quindi, tutti gli Stati del TPM non permanenti vengono persi.</span><span class="sxs-lookup"><span data-stu-id="3a775-111">Thus, all nonpersistent TPM states are lost.</span></span> <span data-ttu-id="3a775-112">Prima di immettere questi Stati, è previsto che il software dell'applicazione si prepari alla perdita di stati TPM volatili.</span><span class="sxs-lookup"><span data-stu-id="3a775-112">Before entering these states, application software is expected to prepare for the loss of volatile TPM states.</span></span> <span data-ttu-id="3a775-113">Quando il sistema torna da uno stato di sospensione, TBS si sincronizza con il TPM in modo che lo stato di TBS sia coerente con lo stato TPM.</span><span class="sxs-lookup"><span data-stu-id="3a775-113">When the system returns from a sleep state, the TBS synchronizes with the TPM so that the TBS state is consistent with the TPM state.</span></span> <span data-ttu-id="3a775-114">Potrebbe essere necessario riemettere i comandi interrotti dal software dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a775-114">Application software may need to reissue commands that were interrupted.</span></span>

 

 




