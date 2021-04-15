---
title: Tag LST
description: Tag LST
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515748"
---
# <a name="lst-tag"></a><span data-ttu-id="9297b-103">Tag LST</span><span class="sxs-lookup"><span data-stu-id="9297b-103">Lst Tag</span></span>

<span data-ttu-id="9297b-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9297b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9297b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9297b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9297b-106">Ripete l'ultima istruzione pronunciata per il carattere.</span><span class="sxs-lookup"><span data-stu-id="9297b-106">Repeats last spoken statement for the character.</span></span>

</dd> <dt>

<span data-ttu-id="9297b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="9297b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9297b-108">\\**LST**</span><span class="sxs-lookup"><span data-stu-id="9297b-108">\\**Lst**</span></span>\\

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="9297b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="9297b-109">Remarks</span></span>

<span data-ttu-id="9297b-110">Questo tag consente a un carattere di ripetere l'ultima istruzione pronunciata.</span><span class="sxs-lookup"><span data-stu-id="9297b-110">This tag enables a character to repeat its last spoken statement.</span></span> <span data-ttu-id="9297b-111">Questo tag deve essere visualizzato da solo nel metodo [**Speak**](speak-method.md) ; non è possibile includere altri parametri o testo.</span><span class="sxs-lookup"><span data-stu-id="9297b-111">This tag must appear by itself in the [**Speak**](speak-method.md) method; no other text or parameters can be included.</span></span> <span data-ttu-id="9297b-112">Quando il testo parlato viene ripetuto, tutti gli altri tag inclusi nel testo originale vengono ripetuti, ad eccezione dei segnalibri.</span><span class="sxs-lookup"><span data-stu-id="9297b-112">When the spoken text is repeated, any other tags included in the original text are repeated, except for bookmarks.</span></span> <span data-ttu-id="9297b-113">Qualsiasi. WAV e. Vengono ripetuti anche i file LWV inclusi nel testo.</span><span class="sxs-lookup"><span data-stu-id="9297b-113">Any .WAV and .LWV files included in the text are also repeated.</span></span>

 

 




