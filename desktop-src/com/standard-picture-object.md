---
title: Oggetto immagine standard
description: Oggetto immagine standard
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963486"
---
# <a name="standard-picture-object"></a><span data-ttu-id="95f65-103">Oggetto immagine standard</span><span class="sxs-lookup"><span data-stu-id="95f65-103">Standard Picture Object</span></span>

<span data-ttu-id="95f65-104">L'oggetto Picture standard fornisce un'astrazione indipendente dal linguaggio per le immagini GDI: bitmap, icone, metafile e metafile avanzati.</span><span class="sxs-lookup"><span data-stu-id="95f65-104">The standard picture object provides a language-neutral abstraction for GDI images: bitmaps, icons, metafiles, and enhanced metafiles.</span></span> <span data-ttu-id="95f65-105">Come per l'oggetto tipo di carattere standard, il sistema fornisce un'implementazione standard di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="95f65-105">As with the standard font object, the system provides a standard implementation of this object.</span></span> <span data-ttu-id="95f65-106">Le interfacce primarie sono [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) e [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), il secondo derivato da **IDispatch** per fornire l'accesso alle proprietà dell'immagine tramite l'automazione OLE.</span><span class="sxs-lookup"><span data-stu-id="95f65-106">Its primary interfaces are [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), the latter being derived from **IDispatch** to provide access to the picture's properties through OLE automation.</span></span> <span data-ttu-id="95f65-107">Un oggetto immagine viene creato nuovo con [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span><span class="sxs-lookup"><span data-stu-id="95f65-107">A picture object is created new with [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>

<span data-ttu-id="95f65-108">L'oggetto Picture supporta inoltre l'interfaccia in uscita [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) in modo che un client possa determinare quando le proprietà dell'immagine cambiano.</span><span class="sxs-lookup"><span data-stu-id="95f65-108">The picture object also supports the outgoing interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) so that a client can determine when picture properties change.</span></span> <span data-ttu-id="95f65-109">Di conseguenza, l'oggetto immagine supporta anche [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) e un punto di connessione per **IPropertyNotifySink**.</span><span class="sxs-lookup"><span data-stu-id="95f65-109">Accordingly, the picture object also supports [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) and one connection point for **IPropertyNotifySink**.</span></span>

<span data-ttu-id="95f65-110">L'oggetto Picture supporta inoltre [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) in modo che possa salvare e caricare autonomamente da un'istanza di [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="95f65-110">The picture object also supports [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) such that it can save and load itself from an instance of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="95f65-111">Un oggetto che utilizza un oggetto immagine internamente normalmente Salva e carica l'immagine come parte della gestione della persistenza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="95f65-111">An object that uses a picture object internally would normally save and load the picture as part of the object's own persistence handling.</span></span> <span data-ttu-id="95f65-112">La funzione [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) semplifica la creazione di un oggetto immagine in base al contenuto del flusso.</span><span class="sxs-lookup"><span data-stu-id="95f65-112">The [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) function simplifies the creation of a picture object based on stream contents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95f65-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95f65-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95f65-114">Proprietà del controllo</span><span class="sxs-lookup"><span data-stu-id="95f65-114">Control Properties</span></span>](control-properties.md)
</dt> </dl>

 

 