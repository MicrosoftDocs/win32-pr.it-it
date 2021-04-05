---
title: IAgentCharacterEx think
description: IAgentCharacterEx think
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046648"
---
# <a name="iagentcharacterexthink"></a><span data-ttu-id="52323-103">IAgentCharacterEx:: Think</span><span class="sxs-lookup"><span data-stu-id="52323-103">IAgentCharacterEx::Think</span></span>

<span data-ttu-id="52323-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="52323-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="52323-105">Consente di visualizzare il testo del fumetto con il testo specificato.</span><span class="sxs-lookup"><span data-stu-id="52323-105">Displays the character's thought word balloon with the specified text.</span></span>

-   <span data-ttu-id="52323-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="52323-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="52323-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span><span class="sxs-lookup"><span data-stu-id="52323-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="52323-108">Testo da visualizzare nel fumetto di pensiero del carattere.</span><span class="sxs-lookup"><span data-stu-id="52323-108">The text to appear in the character's thought balloon.</span></span>

</dd> <dt>

<span data-ttu-id="52323-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="52323-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="52323-110">Indirizzo di una variabile che riceve l'ID della richiesta di **interazione** .</span><span class="sxs-lookup"><span data-stu-id="52323-110">Address of a variable that receives the **Think** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="52323-111">Come il metodo [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) , il metodo **think** è una richiesta in coda che Visualizza il testo in un fumetto di Word, ad eccezione del fatto che i pensieri vengono visualizzati in un fumetto di pensiero speciale.</span><span class="sxs-lookup"><span data-stu-id="52323-111">Like the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method, the **Think** method is a queued request that displays text in a word balloon, except that thoughts display in a special thought balloon.</span></span> <span data-ttu-id="52323-112">Il fumetto di pensiero supporta solo il tag di controllo vocale segnalibro (**\\ MRK**) e ignora tutti gli altri tag di controllo vocale.</span><span class="sxs-lookup"><span data-stu-id="52323-112">The thought balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="52323-113">A differenza di **IAgentCharacter:: Speak**, il metodo **think** non modifica lo stato di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="52323-113">Unlike **IAgentCharacter::Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="52323-114">Le impostazioni di [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) si applicano anche allo stile dell'aspetto del fumetto di riflessione.</span><span class="sxs-lookup"><span data-stu-id="52323-114">The [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) settings also apply to the appearance style of the thought balloon.</span></span> <span data-ttu-id="52323-115">Ad esempio, è necessario che la proprietà [**Enabled**](enabled-property.md) del fumetto sia **valida** anche per il testo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="52323-115">For example, the balloon's [**Enabled**](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="52323-116">Il Word Breaking automatico dell'agente Microsoft in Word Balloon interrompe le parole usando spazi vuoti (ad esempio, spazio e tabulazione).</span><span class="sxs-lookup"><span data-stu-id="52323-116">Microsoft Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="52323-117">Tuttavia, potrebbe suddividere una parola in modo da adattarla anche al fumetto.</span><span class="sxs-lookup"><span data-stu-id="52323-117">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="52323-118">In lingue quali giapponese, cinese e tailandese, in cui gli spazi non vengono usati per interrompere le parole, inserire un carattere di spazio a larghezza zero Unicode (0x200B) tra i caratteri per definire interruzioni di parola logiche.</span><span class="sxs-lookup"><span data-stu-id="52323-118">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="52323-119">Impostare l'ID lingua del carattere (usando [**IAgentCharacterEx:: SetLanguageID**](iagentcharacterex--setlanguageid.md) prima di usare il metodo [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="52323-119">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="52323-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="52323-120">See Also</span></span>

<span data-ttu-id="52323-121">[**IAgentBalloon:: GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx:: Sestyle**](iagentballoonex--setstyle.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md)</span><span class="sxs-lookup"><span data-stu-id="52323-121">[**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md)</span></span>


 

 