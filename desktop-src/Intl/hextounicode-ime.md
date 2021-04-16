---
description: Rich Edit 3,0 supporta l'IME HexToUnicode, che consente a un utente di eseguire la conversione tra caratteri esadecimali e Unicode usando i tasti di scelta rapida in uno dei due modi.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: IME HexToUnicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88042ce276082755613b28a7e4d070c8b3d695f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530313"
---
# <a name="hextounicode-ime"></a><span data-ttu-id="c26d7-103">IME HexToUnicode</span><span class="sxs-lookup"><span data-stu-id="c26d7-103">HexToUnicode IME</span></span>

<span data-ttu-id="c26d7-104">Rich Edit 3,0 supporta l'IME HexToUnicode, che consente a un utente di eseguire la conversione tra caratteri esadecimali e Unicode usando i tasti di scelta rapida in uno dei due modi.</span><span class="sxs-lookup"><span data-stu-id="c26d7-104">Rich Edit 3.0 supports the HexToUnicode IME, which allows a user to convert between hexadecimal and Unicode characters by using hot keys in one of two ways.</span></span>

<span data-ttu-id="c26d7-105">Utilizzando il primo metodo di conversione, l'utente digita il codice carattere in formato esadecimale e quindi immette ALT + X.</span><span class="sxs-lookup"><span data-stu-id="c26d7-105">Using the first conversion method, the user types the character code in hexadecimal and then enters ALT+X.</span></span> <span data-ttu-id="c26d7-106">L'IME sostituisce le cifre esadecimali che precedono il punto di inserimento con il carattere Unicode.</span><span class="sxs-lookup"><span data-stu-id="c26d7-106">The IME replaces the hexadecimal digits preceding the insertion point with the Unicode character.</span></span> <span data-ttu-id="c26d7-107">Se il tipo di carattere corrente non supporta il codice carattere, viene scelto un tipo di carattere appropriato che lo supporta.</span><span class="sxs-lookup"><span data-stu-id="c26d7-107">If the current font does not support the character code, an appropriate font is chosen that does support it.</span></span> <span data-ttu-id="c26d7-108">Per eseguire la conversione da Unicode ad esadecimale, l'utente immette MAIUSC + ALT + X.</span><span class="sxs-lookup"><span data-stu-id="c26d7-108">To convert from Unicode to hexadecimal, the user enters SHIFT+ALT+X.</span></span> <span data-ttu-id="c26d7-109">Questa voce sostituisce il carattere Unicode che precede il punto di inserimento con le cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="c26d7-109">This entry replaces the Unicode character that precedes the insertion point with the hexadecimal digits.</span></span> <span data-ttu-id="c26d7-110">In particolare, questo metodo consente all'utente di determinare il carattere indicato da un indicatore "glifo mancante".</span><span class="sxs-lookup"><span data-stu-id="c26d7-110">In particular, this method allows the user to determine the character that is indicated by a "missing glyph" indicator.</span></span> <span data-ttu-id="c26d7-111">Se il codice carattere esadecimale segue immediatamente alcuni caratteri esadecimali (non carattere) legittimi, l'utente seleziona le cifre specifiche da convertire prima di digitare ALT + X.</span><span class="sxs-lookup"><span data-stu-id="c26d7-111">If the hexadecimal character code immediately follows some legitimate (noncharacter) hexadecimal characters, the user selects the specific digits to convert before typing ALT+X.</span></span> <span data-ttu-id="c26d7-112">Un problema con questo primo metodo è che ALT + X viene talvolta usato come combinazione di tasti per il comando Exit (ovvero eXit).</span><span class="sxs-lookup"><span data-stu-id="c26d7-112">A problem with this first method is that ALT+X is sometimes used as a key combination for the exit command (that is, eXit).</span></span> <span data-ttu-id="c26d7-113">Ad esempio, in Microsoft Office, questo comando viene visualizzato solo come opzione del menu **file** .</span><span class="sxs-lookup"><span data-stu-id="c26d7-113">For example, in Microsoft Office, this command only appears as an option of the **File** menu.</span></span>

<span data-ttu-id="c26d7-114">Il secondo metodo di conversione tra caratteri esadecimali e Unicode riguarda il tastierino numerico.</span><span class="sxs-lookup"><span data-stu-id="c26d7-114">The second method of converting between hexadecimal and Unicode characters involves the number pad.</span></span> <span data-ttu-id="c26d7-115">Utilizzando questo metodo, l'utente digita ALT + numeri del tastierino numerico (con valori maggiori di 255) per immettere i caratteri Unicode utilizzando valori decimali.</span><span class="sxs-lookup"><span data-stu-id="c26d7-115">Using this method, the user types ALT+NumPad numbers (with values greater than 255) to enter Unicode characters using decimal values.</span></span> <span data-ttu-id="c26d7-116">Questo metodo non è utile come il primo perché l'utente non è in grado di visualizzare le cifre esadecimali digitate.</span><span class="sxs-lookup"><span data-stu-id="c26d7-116">This method is not as useful as the first because the user cannot see what hexadecimal digits have been typed.</span></span> <span data-ttu-id="c26d7-117">Inoltre, l'utente non è in grado di correggere le cifre esadecimali, ad eccezione di immettere nuovamente tutte le cifre.</span><span class="sxs-lookup"><span data-stu-id="c26d7-117">Also, the user cannot correct the hexadecimal digits except by re-entering all the digits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c26d7-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c26d7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c26d7-119">Informazioni su Gestione metodi di input</span><span class="sxs-lookup"><span data-stu-id="c26d7-119">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 



