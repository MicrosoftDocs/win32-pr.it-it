---
title: Controllo ICON
description: Definisce un controllo icona. Questo controllo è un'icona visualizzata in una finestra di dialogo.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Menu di controllo delle icone e altre risorse
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400136395a17f039d552373fa35cba0f3545a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471918"
---
# <a name="icon-control"></a><span data-ttu-id="44dbb-105">Controllo ICON</span><span class="sxs-lookup"><span data-stu-id="44dbb-105">ICON control</span></span>

<span data-ttu-id="44dbb-106">Definisce un controllo icona.</span><span class="sxs-lookup"><span data-stu-id="44dbb-106">Defines an icon control.</span></span> <span data-ttu-id="44dbb-107">Questo controllo è un'icona visualizzata in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="44dbb-107">This control is an icon displayed in a dialog box.</span></span>

<span data-ttu-id="44dbb-108">L'istruzione di controllo **Icon** , che può essere usata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) , definisce l'identificatore di risorsa icona, l'identificatore di controllo icona, la posizione e gli attributi di un controllo.</span><span class="sxs-lookup"><span data-stu-id="44dbb-108">The **ICON** control statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the icon-resource identifier, icon-control identifier, position, and attributes of a control.</span></span>

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="44dbb-109"><span id="text"></span><span id="TEXT"></span>*testo*</span><span class="sxs-lookup"><span data-stu-id="44dbb-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="44dbb-110">Nome di un'icona (non un nome di file) definito altrove nel file di risorse.</span><span class="sxs-lookup"><span data-stu-id="44dbb-110">Name of an icon (not a file name) defined elsewhere in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="44dbb-111"><span id="width"></span><span id="WIDTH"></span>*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="44dbb-111"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="44dbb-112">Questo valore viene ignorato e deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="44dbb-112">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="44dbb-113"><span id="height"></span><span id="HEIGHT"></span>*altezza*</span><span class="sxs-lookup"><span data-stu-id="44dbb-113"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="44dbb-114">Questo valore viene ignorato e deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="44dbb-114">This value is ignored and should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="44dbb-115"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="44dbb-115"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="44dbb-116">Stile del controllo.</span><span class="sxs-lookup"><span data-stu-id="44dbb-116">Control style.</span></span> <span data-ttu-id="44dbb-117">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="44dbb-117">This parameter is optional.</span></span> <span data-ttu-id="44dbb-118">L'unico valore che è possibile specificare è lo stile dell' **\_ icona SS** .</span><span class="sxs-lookup"><span data-stu-id="44dbb-118">The only value that can be specified is the **SS\_ICON** style.</span></span> <span data-ttu-id="44dbb-119">Si tratta dello stile predefinito se questo parametro è specificato o meno.</span><span class="sxs-lookup"><span data-stu-id="44dbb-119">This is the default style whether this parameter is specified or not.</span></span>

</dd> </dl>

<span data-ttu-id="44dbb-120">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="44dbb-120">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="44dbb-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="44dbb-121">Examples</span></span>

<span data-ttu-id="44dbb-122">Questo esempio definisce un controllo Icon il cui identificatore di icona è 901 e il cui nome è l'icona:</span><span class="sxs-lookup"><span data-stu-id="44dbb-122">This example defines an icon control whose icon identifier is 901 and whose name is myicon:</span></span>

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a><span data-ttu-id="44dbb-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44dbb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44dbb-124">**ICONA**</span><span class="sxs-lookup"><span data-stu-id="44dbb-124">**ICON**</span></span>](icon-resource.md)
</dt> </dl>

 

 




