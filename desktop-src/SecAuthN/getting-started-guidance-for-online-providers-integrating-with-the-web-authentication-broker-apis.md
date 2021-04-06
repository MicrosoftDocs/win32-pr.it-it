---
description: Linee guida per gli sviluppatori Web e i provider online per creare pagine Web personalizzate per le API del broker di autenticazione Web di Windows 8 per Single Sign-On (SSO).
ms.assetid: E2AECE26-9649-41CB-9808-4F8171C707C3
title: Guida introduttiva per i provider online integrazione con le API del broker di autenticazione Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842f3c562d2ad288efaecec82f8da8ca771886a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883909"
---
# <a name="getting-started-guidance-for-online-providers-integrating-with-the-web-authentication-broker-apis"></a><span data-ttu-id="fbd23-103">Guida introduttiva per i provider online integrazione con le API del broker di autenticazione Web</span><span class="sxs-lookup"><span data-stu-id="fbd23-103">Getting started guidance for online providers integrating with the Web Authentication Broker APIs</span></span>

<span data-ttu-id="fbd23-104">In questa sezione vengono illustrati gli sviluppatori Web e i provider online per la creazione di pagine Web personalizzate per le API del broker di autenticazione Web di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fbd23-104">This section guides web developers and online providers for creating web pages tailored for the Windows 8 Web Authentication Broker APIs.</span></span> <span data-ttu-id="fbd23-105">Fornisce le raccomandazioni visive e interattive per un'esperienza utente end-to-end della pagina Web e come abilitare le funzionalità di Single Sign-On (SSO).</span><span class="sxs-lookup"><span data-stu-id="fbd23-105">It provides the visual and interactive recommendations for an end-to-end user experience of the web page as well as how to enable single sign-on (SSO) capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fbd23-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="fbd23-106">In this section</span></span>



| <span data-ttu-id="fbd23-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="fbd23-107">Topic</span></span>                                                                                                     | <span data-ttu-id="fbd23-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbd23-108">Description</span></span>                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fbd23-109">Considerazioni relative allo sviluppo di pagine Web</span><span class="sxs-lookup"><span data-stu-id="fbd23-109">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)<br/> | <span data-ttu-id="fbd23-110">Il broker di autenticazione Web si basa sulle stesse tecnologie di Internet Explorer in Windows.</span><span class="sxs-lookup"><span data-stu-id="fbd23-110">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="fbd23-111">Tuttavia, a causa di uno scopo speciale di questo componente alcune funzionalità di Internet Explorer sono state disabilitate o bloccate a una configurazione specifica.</span><span class="sxs-lookup"><span data-stu-id="fbd23-111">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <br/> |
| [<span data-ttu-id="fbd23-112">Come personalizzare gli elementi dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="fbd23-112">How to customize the UI elements</span></span>](how-to-customize-the-ui-elements.md)<br/>                       | <span data-ttu-id="fbd23-113">Una pagina Web Personalizza l'interfaccia utente con il titolo, l'icona e il colore dell'intestazione usando i tag dei metadati definiti nella pagina Web.</span><span class="sxs-lookup"><span data-stu-id="fbd23-113">A web page customizes the user interface (UI) with the title, icon, and header color by using metadata tags defined on the web page.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="fbd23-114">Esercitazione per l'autenticazione di pagine Web</span><span class="sxs-lookup"><span data-stu-id="fbd23-114">Tutorial for authenticating web pages</span></span>](tutorial-for-authenticating-web-pages.md)<br/>             |                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="fbd23-115">Problemi relativi all'autenticazione Web</span><span class="sxs-lookup"><span data-stu-id="fbd23-115">Web authentication problems</span></span>](web-authentication-problems.md)<br/>                                 | <span data-ttu-id="fbd23-116">In questo argomento vengono descritti i suggerimenti per la risoluzione dei problemi relativi all'utilizzo delle API del broker di autenticazione Web per le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="fbd23-116">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="fbd23-117">Domande frequenti sul broker di autenticazione Web</span><span class="sxs-lookup"><span data-stu-id="fbd23-117">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)<br/>                     | <span data-ttu-id="fbd23-118">Domande frequenti sul broker di autenticazione Web.</span><span class="sxs-lookup"><span data-stu-id="fbd23-118">Frequently asked questions for Web Authentication Broker.</span></span><br/>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="fbd23-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fbd23-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fbd23-120">[Panoramica di broker di autenticazione Web](/previous-versions/windows/apps/hh750287(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="fbd23-120">[Web authentication broker overview](/previous-versions/windows/apps/hh750287(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="fbd23-121">App di esempio SDK Web Authentication broker</span><span class="sxs-lookup"><span data-stu-id="fbd23-121">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="fbd23-122">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="fbd23-122">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

