---
title: Sezione Marquee
description: Sezione Marquee
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Interfacce di Windows Media Player Mobile, Marquees
- interfacce, Marquee
- creazione di interfacce, sezione Marquee
- scrittura di codice per interfacce, sezione Marquee
- Marquees in Skins, sezione Marquee
- file di definizione dell'interfaccia, sezione Marquee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714518"
---
# <a name="marquee-section"></a><span data-ttu-id="f1d8d-109">Sezione Marquee</span><span class="sxs-lookup"><span data-stu-id="f1d8d-109">Marquee Section</span></span>

<span data-ttu-id="f1d8d-110">La sezione Marquee contiene informazioni sulla casella di testo Marquee, che consente di visualizzare il testo di scorrimento:</span><span class="sxs-lookup"><span data-stu-id="f1d8d-110">The Marquee section contains information about the marquee text box, which will display scrolling text:</span></span>


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



<span data-ttu-id="f1d8d-111">Verrà visualizzato il titolo e l'autore dell'elemento multimediale corrente anche se è possibile visualizzare qualsiasi tipo di testo nella casella di selezione.</span><span class="sxs-lookup"><span data-stu-id="f1d8d-111">This will display the title and author of the current media item although you can display any text type in the marquee.</span></span> <span data-ttu-id="f1d8d-112">È ad esempio possibile includere anche filename, status e playlist nel Marquee.</span><span class="sxs-lookup"><span data-stu-id="f1d8d-112">For example, you could also include Filename, Status, and Playlist in your marquee.</span></span>

> [!Note]  
> <span data-ttu-id="f1d8d-113">Per mantenere la compatibilità con le versioni di Windows Media Player Mobile precedenti a Windows Media Player 10 Mobile, l'utilizzo di "Marquis" in un file di definizione dell'interfaccia personalizzata è ancora considerato valido.</span><span class="sxs-lookup"><span data-stu-id="f1d8d-113">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="f1d8d-114">Per ulteriori informazioni sulla sezione Marquee, vedere [Marquee](marquee.md) in the Skin Reference.</span><span class="sxs-lookup"><span data-stu-id="f1d8d-114">For more about the Marquee section, see [Marquee](marquee.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1d8d-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1d8d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1d8d-116">**Scrittura del codice**</span><span class="sxs-lookup"><span data-stu-id="f1d8d-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




