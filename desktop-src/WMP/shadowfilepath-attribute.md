---
title: Attributo ShadowFilePath
description: L'attributo ShadowFilePath è il percorso completo di un file shadow.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- Attributo ShadowFilePath Windows Media Player
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327365"
---
# <a name="shadowfilepath-attribute"></a><span data-ttu-id="ed448-104">Attributo ShadowFilePath</span><span class="sxs-lookup"><span data-stu-id="ed448-104">ShadowFilePath Attribute</span></span>

<span data-ttu-id="ed448-105">L'attributo **ShadowFilePath** è il percorso completo di un file shadow.</span><span class="sxs-lookup"><span data-stu-id="ed448-105">The **ShadowFilePath** attribute is the fully qualified path to a shadow file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ed448-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="ed448-106">Applies To</span></span>

-   [<span data-ttu-id="ed448-107">Elementi audio</span><span class="sxs-lookup"><span data-stu-id="ed448-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="ed448-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed448-108">Remarks</span></span>

<span data-ttu-id="ed448-109">Un *file shadow* viene creato come parte di una conversione del formato di file.</span><span class="sxs-lookup"><span data-stu-id="ed448-109">A *shadow file* is created as part of a file format conversion.</span></span> <span data-ttu-id="ed448-110">Si tratta della copia di un file usato dal giocatore quando l'utente Sincronizza il contenuto dal computer a un dispositivo che richiede che il contenuto sia nel formato di file originale.</span><span class="sxs-lookup"><span data-stu-id="ed448-110">It is the copy of a file that the Player uses when the user syncs content from the computer to a device that requires the content to be in the original file format.</span></span> <span data-ttu-id="ed448-111">Questo attributo è impostato per il file convertito in modo che punti al percorso del file shadow.</span><span class="sxs-lookup"><span data-stu-id="ed448-111">This attribute is set for the converted file to point to the location of the shadow file.</span></span>

<span data-ttu-id="ed448-112">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ed448-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed448-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed448-113">Requirements</span></span>



| <span data-ttu-id="ed448-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed448-114">Requirement</span></span> | <span data-ttu-id="ed448-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ed448-115">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="ed448-116">Versione</span><span class="sxs-lookup"><span data-stu-id="ed448-116">Version</span></span><br/> | <span data-ttu-id="ed448-117">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="ed448-117">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed448-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed448-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed448-119">**Informazioni sul processo di conversione**</span><span class="sxs-lookup"><span data-stu-id="ed448-119">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="ed448-120">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="ed448-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





