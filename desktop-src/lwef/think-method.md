---
title: Metodo think
description: Metodo think
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872426"
---
# <a name="think-method"></a><span data-ttu-id="4d42d-103">Metodo think</span><span class="sxs-lookup"><span data-stu-id="4d42d-103">Think Method</span></span>

<span data-ttu-id="4d42d-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4d42d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4d42d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="4d42d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4d42d-106">Consente di visualizzare il testo specificato per il carattere specificato in un fumetto di parola "pensata".</span><span class="sxs-lookup"><span data-stu-id="4d42d-106">Displays the specified text for the specified character in a "thought" word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="4d42d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="4d42d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4d42d-108">\*agente ***. Caratteri ("*** CharacterID \* \* *").* \*  \[ *Testo* interazione\]</span><span class="sxs-lookup"><span data-stu-id="4d42d-108">*agent ***.Characters ("*** CharacterID\*\*\*").Think*\* \[*Text*\]</span></span>



| <span data-ttu-id="4d42d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="4d42d-109">Part</span></span>   | <span data-ttu-id="4d42d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d42d-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="4d42d-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="4d42d-111">*Text*</span></span> | <span data-ttu-id="4d42d-112">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4d42d-112">Optional.</span></span> <span data-ttu-id="4d42d-113">Stringa che specifica l'output del pensiero del carattere.</span><span class="sxs-lookup"><span data-stu-id="4d42d-113">A string that specifies the character's thought output.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d42d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d42d-114">Remarks</span></span>

<span data-ttu-id="4d42d-115">Analogamente al metodo [**Speak**](speak-method.md) , il metodo **think** è una richiesta in coda che Visualizza il testo in un fumetto di Word, ad eccezione del fatto che il fumetto **think** Word differisce visivamente.</span><span class="sxs-lookup"><span data-stu-id="4d42d-115">Like the [**Speak**](speak-method.md) method, the **Think** method is a queued request that displays text in a word balloon, except that the **Think** word balloon differs visually.</span></span> <span data-ttu-id="4d42d-116">Inoltre, il fumetto supporta solo il tag di controllo vocale segnalibro (**\\ MRK**) e ignora tutti gli altri tag di controllo vocale.</span><span class="sxs-lookup"><span data-stu-id="4d42d-116">In addition, the balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="4d42d-117">Diversamente da **Speak**, il metodo **think** non modifica lo stato di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="4d42d-117">Unlike **Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="4d42d-118">Le proprietà dell'oggetto [**Balloon**](/windows/desktop/lwef/the-balloon-object) influiscono sull'output dei metodi [**Speak**](speak-method.md) e **think** .</span><span class="sxs-lookup"><span data-stu-id="4d42d-118">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object's properties affect the output of both the [**Speak**](speak-method.md) and **Think** methods.</span></span> <span data-ttu-id="4d42d-119">La proprietà [**Enabled**](enabled-property.md) dell'oggetto **Balloon** , ad esempio, deve essere **true** per visualizzare il testo.</span><span class="sxs-lookup"><span data-stu-id="4d42d-119">For example, the **Balloon** object's [**Enabled**](enabled-property.md) property must be **True** for text to display.</span></span>

<span data-ttu-id="4d42d-120">Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="4d42d-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="4d42d-121">Inoltre, se il file non è stato caricato, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **richiesta** su "failed" con un numero di codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="4d42d-121">In addition, if the file has not been loaded, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="4d42d-122">Il Word Breaking automatico dell'agente in Word Balloon interrompe le parole usando spazi vuoti (ad esempio, spazio o tabulazione).</span><span class="sxs-lookup"><span data-stu-id="4d42d-122">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="4d42d-123">Tuttavia, se non è possibile, potrebbe interrompere una parola per adattarla al fumetto.</span><span class="sxs-lookup"><span data-stu-id="4d42d-123">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="4d42d-124">In lingue quali giapponese, cinese e tailandese, in cui gli spazi non vengono usati per interrompere le parole, inserire un carattere di spazio a larghezza zero Unicode (0x200B) tra i caratteri per definire interruzioni di parola logiche.</span><span class="sxs-lookup"><span data-stu-id="4d42d-124">In languages like Japanese, Chinese, and Thai where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="4d42d-125">Impostare l'ID lingua del carattere prima di utilizzare il metodo [**Speak**](speak-method.md) per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="4d42d-125">Set the character's language ID before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 