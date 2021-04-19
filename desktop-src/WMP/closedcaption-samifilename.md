---
title: ClosedCaption.SAMIFileName
description: La proprietà SAMIFileName specifica o Recupera il nome del file contenente le informazioni necessarie per la didascalia chiusa.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- Media Player Windows ClosedCaption. SAMIFileName
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326732"
---
# <a name="closedcaptionsamifilename"></a><span data-ttu-id="a33e3-104">ClosedCaption.SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="a33e3-104">ClosedCaption.SAMIFileName</span></span>

<span data-ttu-id="a33e3-105">La proprietà **SAMIFileName** specifica o Recupera il nome del file contenente le informazioni necessarie per la didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="a33e3-105">The **SAMIFileName** property specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a><span data-ttu-id="a33e3-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="a33e3-106">Possible Values</span></span>

<span data-ttu-id="a33e3-107">Questa proprietà è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a33e3-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a33e3-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="a33e3-108">Remarks</span></span>

<span data-ttu-id="a33e3-109">Il file di interscambio multimediale accessibile sincronizzato (SAMI) deve usare un'estensione del nome file. SMI o. Sami.</span><span class="sxs-lookup"><span data-stu-id="a33e3-109">The Synchronized Accessible Media Interchange (SAMI) file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="a33e3-110">Se non si specifica un valore per **SAMIFileName**, questa proprietà recupera una stringa contenente il nome file o l'URL associato all'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="a33e3-110">If you don't specify a value for **SAMIFileName**, this property retrieves a string containing the file name or URL associated with the current media item.</span></span> <span data-ttu-id="a33e3-111">Questa associazione può verificarsi quando un file SAMI viene specificato con il parametro dell'URL *Sami* oppure automaticamente quando il file Sami ha lo stesso nome del file multimediale digitale, ad eccezione dell'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="a33e3-111">This association can occur when a SAMI file is specified using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file name (except for the file name extension).</span></span> <span data-ttu-id="a33e3-112">Se al supporto corrente non è associato alcun file SAMI, questa proprietà recupera una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="a33e3-112">If there is no SAMI file associated with the current media, this property retrieves an empty string ("").</span></span>

<span data-ttu-id="a33e3-113">Quando si specifica un valore per **SAMIFileName**, tale valore viene mantenuto fino a quando non si specifica un nuovo valore o finché non viene aperto un nuovo elemento multimediale con il parametro *Sami* URL.</span><span class="sxs-lookup"><span data-stu-id="a33e3-113">Once you specify a value for **SAMIFileName**, that value persists until you specify a new value (or until a new media item is opened using the *sami* URL parameter).</span></span> <span data-ttu-id="a33e3-114">Pertanto, è necessario specificare un nuovo valore per questa proprietà prima di riprodurre ogni nuovo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a33e3-114">Therefore, you must specify a new value for this property before you play each new media item.</span></span> <span data-ttu-id="a33e3-115">In questo modo, il nuovo valore di **SAMIFileName** verrà applicato quando viene aperto il successivo elemento multimediale (o quando il *lettore*.**Close** viene chiamato).</span><span class="sxs-lookup"><span data-stu-id="a33e3-115">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when *Player*.**close** is called).</span></span> <span data-ttu-id="a33e3-116">La specifica di un nuovo valore per **SAMIFileName** non ha alcun effetto sui supporti correnti.</span><span class="sxs-lookup"><span data-stu-id="a33e3-116">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="a33e3-117">Per fare in modo che Windows Media Player ritorni a utilizzando il file SAMI associato a un particolare elemento multimediale, specificare un valore per **SAMIFileName** uguale a una stringa vuota ("") prima di riprodurre il successivo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a33e3-117">To cause Windows Media Player to return to using the SAMI file associated with a particular media item, specify a value for **SAMIFileName** equal to an empty string ("") before you play the next media item.</span></span>

<span data-ttu-id="a33e3-118">**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura e restituisce sempre una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="a33e3-118">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="a33e3-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="a33e3-119">Examples</span></span>

<span data-ttu-id="a33e3-120">Nei tre esempi di JScript seguenti viene utilizzato *ClosedCaption*. **SAMIFileName** per specificare il nome di un file di testo del titolo chiuso.</span><span class="sxs-lookup"><span data-stu-id="a33e3-120">The following three JScript examples use *ClosedCaption*.**SAMIFileName** to specify the name of a closed caption text file.</span></span> <span data-ttu-id="a33e3-121">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a33e3-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a><span data-ttu-id="a33e3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a33e3-122">Requirements</span></span>



| <span data-ttu-id="a33e3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33e3-123">Requirement</span></span> | <span data-ttu-id="a33e3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a33e3-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a33e3-125">Versione</span><span class="sxs-lookup"><span data-stu-id="a33e3-125">Version</span></span><br/> | <span data-ttu-id="a33e3-126">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="a33e3-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a33e3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a33e3-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="a33e3-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a33e3-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a33e3-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a33e3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33e3-130">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="a33e3-130">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="a33e3-131">**Oggetto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="a33e3-131">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="a33e3-132">**Player. Close**</span><span class="sxs-lookup"><span data-stu-id="a33e3-132">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





