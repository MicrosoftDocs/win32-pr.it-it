---
title: Progetto personalizzato
description: Il progetto personalizzato non è un controllo comune; si tratta di un servizio che molti controlli comuni forniscono.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5184d06dbb8e04185bf12a43c6c71dd96b933a6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955271"
---
# <a name="custom-draw"></a><span data-ttu-id="7e970-103">Progetto personalizzato</span><span class="sxs-lookup"><span data-stu-id="7e970-103">Custom Draw</span></span>

<span data-ttu-id="7e970-104">Il progetto personalizzato non è un controllo comune; si tratta di un servizio che molti controlli comuni forniscono.</span><span class="sxs-lookup"><span data-stu-id="7e970-104">Custom draw is not a common control; it is a service that many common controls provide.</span></span> <span data-ttu-id="7e970-105">Il servizio di personalizzazione personalizzato consente a un'applicazione una maggiore flessibilità nella personalizzazione dell'aspetto di un controllo.</span><span class="sxs-lookup"><span data-stu-id="7e970-105">The custom draw service allows an application greater flexibility in customizing a control's appearance.</span></span> <span data-ttu-id="7e970-106">L'applicazione può sfruttare le notifiche di traccia personalizzate per modificare facilmente il tipo di carattere usato per visualizzare gli elementi o per tracciare manualmente un elemento senza dover eseguire un Owner Draw completo.</span><span class="sxs-lookup"><span data-stu-id="7e970-106">Your application can harness custom draw notifications to easily change the font used to display items or manually draw an item without having to do a full owner draw.</span></span>

<span data-ttu-id="7e970-107">Questa sezione contiene informazioni sugli elementi di programmazione usati con il progetto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7e970-107">This section contains information about the programming elements used with custom draw.</span></span>

## <a name="overviews"></a><span data-ttu-id="7e970-108">Cenni preliminari</span><span class="sxs-lookup"><span data-stu-id="7e970-108">Overviews</span></span>



| <span data-ttu-id="7e970-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="7e970-109">Topic</span></span>                                      | <span data-ttu-id="7e970-110">Contenuto</span><span class="sxs-lookup"><span data-stu-id="7e970-110">Contents</span></span>                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e970-111">Informazioni sul progetto personalizzato</span><span class="sxs-lookup"><span data-stu-id="7e970-111">About Custom Draw</span></span>](about-custom-draw.md) | <span data-ttu-id="7e970-112">Questa sezione contiene informazioni generali sulla funzionalità di personalizzazione personalizzata e fornisce una panoramica concettuale del modo in cui un'applicazione può supportare il progetto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7e970-112">This section contains general information about custom draw functionality and provides a conceptual overview of how an application can support custom draw.</span></span><br/> |
| [<span data-ttu-id="7e970-113">Uso di un progetto personalizzato</span><span class="sxs-lookup"><span data-stu-id="7e970-113">Using Custom Draw</span></span>](using-custom-draw.md) | <span data-ttu-id="7e970-114">Questa sezione contiene esempi che illustrano come implementare un progetto personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7e970-114">This section contains examples that demonstrate how to implement custom draw.</span></span> <br/>                                                                              |



 

## <a name="notifications"></a><span data-ttu-id="7e970-115">Notifiche</span><span class="sxs-lookup"><span data-stu-id="7e970-115">Notifications</span></span>



| <span data-ttu-id="7e970-116">Argomento</span><span class="sxs-lookup"><span data-stu-id="7e970-116">Topic</span></span>                               | <span data-ttu-id="7e970-117">Contenuto</span><span class="sxs-lookup"><span data-stu-id="7e970-117">Contents</span></span>                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e970-118">\_CUSTOMDRAW Nm</span><span class="sxs-lookup"><span data-stu-id="7e970-118">NM\_CUSTOMDRAW</span></span>](nm-customdraw.md) | <span data-ttu-id="7e970-119">Notifica alla finestra padre di un controllo informazioni sulle operazioni di disegno personalizzate.</span><span class="sxs-lookup"><span data-stu-id="7e970-119">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="7e970-120">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7e970-120">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

## <a name="structures"></a><span data-ttu-id="7e970-121">Strutture</span><span class="sxs-lookup"><span data-stu-id="7e970-121">Structures</span></span>



| <span data-ttu-id="7e970-122">Argomento</span><span class="sxs-lookup"><span data-stu-id="7e970-122">Topic</span></span>                                | <span data-ttu-id="7e970-123">Contenuto</span><span class="sxs-lookup"><span data-stu-id="7e970-123">Contents</span></span>                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e970-124">**NMCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="7e970-124">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | <span data-ttu-id="7e970-125">Contiene informazioni specifiche di un codice di notifica [ \_ CUSTOMDRAW Nm](nm-customdraw.md) .</span><span class="sxs-lookup"><span data-stu-id="7e970-125">Contains information specific to an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code.</span></span><br/> |



 

 

 





