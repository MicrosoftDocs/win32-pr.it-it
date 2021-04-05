---
title: Barra della lingua (applicazioni TSF)
description: Un'applicazione non può aggiungere elementi alla barra della lingua; solo un servizio di testo può aggiungere elementi alla barra della lingua.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Framework servizi di testo (TSF), barra della lingua
- TSF (Framework dei servizi di testo), barra della lingua
- Applicazioni abilitate per TSF, barra della lingua
- barra della lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef227b29c8b481bfaefc4a218305ba8974fe54e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873249"
---
# <a name="language-bar-tsf-applications"></a><span data-ttu-id="48ce4-107">Barra della lingua (applicazioni TSF)</span><span class="sxs-lookup"><span data-stu-id="48ce4-107">Language Bar (TSF Applications)</span></span>

<span data-ttu-id="48ce4-108">Un'applicazione non può aggiungere elementi alla barra della lingua; solo un servizio di testo può aggiungere elementi alla barra della lingua.</span><span class="sxs-lookup"><span data-stu-id="48ce4-108">An application cannot add items to the language bar; only a text service can add items to the language bar.</span></span> <span data-ttu-id="48ce4-109">Un'applicazione può influire sulla modalità di visualizzazione di determinati elementi sulla barra della lingua.</span><span class="sxs-lookup"><span data-stu-id="48ce4-109">An application can affect how certain items on the language bar appear.</span></span>

<span data-ttu-id="48ce4-110">Il raggruppamento di [ \_ \_ \_ DICTATIONSTAT](predefined-compartments.md) per la voce del raggruppamento GUID viene usato per indicare il tipo di input vocale che l'applicazione può accettare: input di testo diretto (dettatura) e/o comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="48ce4-110">The [GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT](predefined-compartments.md) compartment is used to indicate the type of speech input that the application can accept: direct text input (dictation) and/or voice commands.</span></span> <span data-ttu-id="48ce4-111">Per impostazione predefinita, la dettatura è abilitata e il comando Voice è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="48ce4-111">By default, dictation is enabled and voice command is disabled.</span></span> <span data-ttu-id="48ce4-112">Se l'applicazione è in grado di accettare comandi vocali, deve impostare il valore [ \_ \_ abilitato per il comando tf](speech-recognition-constants.md) nel raggruppamento DICTATIONSTAT del dialogo del raggruppamento dei GUID \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="48ce4-112">If the application can accept voice commands, it should set the [TF\_COMMANDING\_ENABLED](speech-recognition-constants.md) value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="48ce4-113">Se l'applicazione è in grado di accettare la dettatura, deve impostare il \_ \_ valore abilitato per la dettatura di TF nel raggruppamento DICTATIONSTAT della voce del raggruppamento GUID \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="48ce4-113">If the application can accept dictation, it should set the TF\_DICTATION\_ENABLED value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="48ce4-114">La \_ dettatura del TF \_ o il \_ comando tf \_ sul valore di questo raggruppamento determina l'input vocale della modalità (dettatura o comando) attualmente in.</span><span class="sxs-lookup"><span data-stu-id="48ce4-114">The TF\_DICTATION\_ON or TF\_COMMANDING\_ON value of this compartment determines which mode (dictation or command) speech input is currently in.</span></span>

<span data-ttu-id="48ce4-115">Se l'applicazione supporta l'archiviazione permanente dei dati delle proprietà, è necessario impostare il raggruppamento [GUID \_ \_ PERSISTMENUENABLED](predefined-compartments.md) raggruppamento su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="48ce4-115">If the application supports persistent storage of property data, it should set the [GUID\_COMPARTMENT\_PERSISTMENUENABLED](predefined-compartments.md) compartment to a nonzero value.</span></span> <span data-ttu-id="48ce4-116">Questo fa sì che il servizio di testo vocale consenta la voce di menu **Salva dati vocali** .</span><span class="sxs-lookup"><span data-stu-id="48ce4-116">This causes the speech text service to enable the **Save Speech Data** menu item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48ce4-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48ce4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48ce4-118">Come configurare il Framework dei servizi di testo</span><span class="sxs-lookup"><span data-stu-id="48ce4-118">How To Set Up Text Services Framework</span></span>](how-to-set-up-tsf.md)
</dt> <dt>

[<span data-ttu-id="48ce4-119">Barra della lingua (servizi di testo)</span><span class="sxs-lookup"><span data-stu-id="48ce4-119">Language Bar (Text Services)</span></span>](language-bar.md)
</dt> </dl>

 

 




