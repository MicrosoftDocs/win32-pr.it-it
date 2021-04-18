---
title: Connessione Web Desktop remoto
description: Connessione Web Desktop remoto è un'applicazione Web costituita da un controllo ActiveX e da una pagina di connessione di esempio.
ms.assetid: f9d252b0-205a-47df-9eca-d5744c09e079
ms.tgt_platform: multiple
keywords:
- Connessione Web Desktop remoto Servizi Desktop remoto
- Servizi Desktop remoto di Remote Desktop Protocol (RDP), Connessione Web Desktop remoto Panoramica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bb1e8f562e3e5c47c6050f550fe3c7090446be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300042"
---
# <a name="remote-desktop-web-connection"></a><span data-ttu-id="82085-105">Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="82085-105">Remote Desktop Web Connection</span></span>

<span data-ttu-id="82085-106">Connessione Web Desktop remoto è un'applicazione Web costituita da un controllo ActiveX e da una pagina di connessione di esempio.</span><span class="sxs-lookup"><span data-stu-id="82085-106">Remote Desktop Web Connection is a web application consisting of an ActiveX control and a sample connection page.</span></span> <span data-ttu-id="82085-107">Quando si distribuisce Connessione Web Desktop remoto in un server Web, è possibile fornire la connettività client ai server di host sessione Desktop remoto (host sessione Desktop remoto) e ad altri computer che utilizzano Internet Explorer e TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="82085-107">When you deploy Remote Desktop Web Connection on a web server, you can provide client connectivity to Remote Desktop Session Host (RD Session Host) servers and other computers using Internet Explorer and TCP/IP.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="82085-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="82085-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="82085-109">Requisiti per Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="82085-109">Requirements for Remote Desktop Web Connection</span></span>](requirements-for-remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="82085-110">Elenca i requisiti per un Connessione Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="82085-110">Lists the requirements for a Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="82085-111">Canali virtuali tramite script</span><span class="sxs-lookup"><span data-stu-id="82085-111">Scriptable virtual channels</span></span>](scriptable-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="82085-112">Vengono descritte le modifiche apportate al modello di programmazione per l'implementazione di applicazioni di canale virtuale fornite dal Client avanzato di Servizi terminal (TSAC).</span><span class="sxs-lookup"><span data-stu-id="82085-112">Describes changes to the programming model for implementing virtual channel applications that are provided by the Terminal Services Advanced Client (TSAC).</span></span>

</dd> </dl>

<span data-ttu-id="82085-113">Il materiale di riferimento per Connessione Web Desktop remoto è incluso nella sezione [connessione Web Desktop remoto Reference](remote-desktop-web-connection-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="82085-113">The reference material for Remote Desktop Web Connection is included in the [Remote Desktop Web Connection Reference](remote-desktop-web-connection-reference.md) section.</span></span>

<span data-ttu-id="82085-114">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="82085-114">For more information, see these topics:</span></span>

-   [<span data-ttu-id="82085-115">Implementazione di canali virtuali tramite script con Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="82085-115">Implementing Scriptable Virtual Channels Using Remote Desktop Web Connection</span></span>](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
-   [<span data-ttu-id="82085-116">Incorporamento del controllo ActiveX Desktop remoto in una pagina Web</span><span class="sxs-lookup"><span data-stu-id="82085-116">Embedding the Remote Desktop ActiveX Control in a Webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
-   <span data-ttu-id="82085-117">[Download e utilizzo del controllo ActiveX Desktop remoto](/previous-versions//aa380808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82085-117">[Downloading and Using the Remote Desktop ActiveX Control](/previous-versions//aa380808(v=vs.85))</span></span>
-   [<span data-ttu-id="82085-118">Uso del controllo ActiveX Desktop remoto con i canali virtuali</span><span class="sxs-lookup"><span data-stu-id="82085-118">Using the Remote Desktop ActiveX Control with Virtual Channels</span></span>](using-the-remote-desktop-activex-control-with-virtual-channels.md)
-   [<span data-ttu-id="82085-119">Fornire la sicurezza del client RDP</span><span class="sxs-lookup"><span data-stu-id="82085-119">Providing for RDP Client Security</span></span>](providing-for-rdp-client-security.md)
-   [<span data-ttu-id="82085-120">Disabilitazione delle funzionalità di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="82085-120">Disabling Remote Desktop Services Features</span></span>](disabling-terminal-services-features.md)

## <a name="installing-remote-desktop-web-connection"></a><span data-ttu-id="82085-121">Installazione di Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="82085-121">Installing Remote Desktop Web Connection</span></span>

<span data-ttu-id="82085-122">La procedura seguente consente di installare il controllo ActiveX Desktop remoto e la pagina Web di esempio nella directory% SystemRoot% \\ Web \\ nella tsweb.</span><span class="sxs-lookup"><span data-stu-id="82085-122">The following steps install the Remote Desktop ActiveX control and sample webpage to the %systemroot%\\Web\\Tsweb directory.</span></span> <span data-ttu-id="82085-123">Condividono la pagina Web nella directory nella TSWeb del server, ad esempio, in https://*MyServer*/tsweb.</span><span class="sxs-lookup"><span data-stu-id="82085-123">They share the webpage in the Tsweb directory on your server, for example, at https://*MyServer*/tsweb.</span></span> <span data-ttu-id="82085-124">Il controllo (Msrdp. ocx) e il codice Connessione Web Desktop remoto si trovano in Msrdp.cab.</span><span class="sxs-lookup"><span data-stu-id="82085-124">The control (Msrdp.ocx) and the Remote Desktop Web Connection code are located in Msrdp.cab.</span></span>

<span data-ttu-id="82085-125">**Per installare Connessione Web Desktop remoto**</span><span class="sxs-lookup"><span data-stu-id="82085-125">**To install Remote Desktop Web Connection**</span></span>

1.  <span data-ttu-id="82085-126">Nell'elemento Installazione applicazioni nel pannello di controllo, in installazione componenti di Windows, installare Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="82085-126">In the Add/Remove Programs item in Control Panel, under Add/Remove Windows Components, install Microsoft Internet Information Services (IIS).</span></span>
2.  <span data-ttu-id="82085-127">Installare il sottocomponente servizio World Wide Web di IIS.</span><span class="sxs-lookup"><span data-stu-id="82085-127">Install the World Wide Web Service subcomponent of IIS.</span></span>
3.  <span data-ttu-id="82085-128">Installare il sottocomponente Connessione Web Desktop remoto di World Wide Web servizio.</span><span class="sxs-lookup"><span data-stu-id="82085-128">Install the Remote Desktop Web Connection subcomponent of World Wide Web Service.</span></span>

<span data-ttu-id="82085-129">Per una descrizione della pagina Web inclusa con l'installazione di Connessione Web Desktop remoto, vedere [la pagina Web di esempio inclusa nel controllo ActiveX Desktop remoto](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span><span class="sxs-lookup"><span data-stu-id="82085-129">For a description of the webpage that is included with the installation of Remote Desktop Web Connection, see [Sample Webpage Included with the Remote Desktop ActiveX Control](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span></span>

 

 