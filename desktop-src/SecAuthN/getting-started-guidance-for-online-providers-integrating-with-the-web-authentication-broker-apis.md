---
description: Linee guida per sviluppatori Web e provider online per creare pagine Web personalizzate per le API di Windows 8 Web Authentication Broker per le funzionalità Single Sign-On (SSO).
ms.assetid: E2AECE26-9649-41CB-9808-4F8171C707C3
title: Guida introduttiva per i provider online che si integrano con le API di Web Authentication Broker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bf0ce59cd92e32264823861aaef44e90b4f2c0
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353634"
---
# <a name="getting-started-guidance-for-online-providers-integrating-with-the-web-authentication-broker-apis"></a><span data-ttu-id="86bb3-103">Guida introduttiva per i provider online che si integrano con le API di Web Authentication Broker</span><span class="sxs-lookup"><span data-stu-id="86bb3-103">Getting started guidance for online providers integrating with the Web Authentication Broker APIs</span></span>

<span data-ttu-id="86bb3-104">Questa sezione guida gli sviluppatori Web e i provider online per la creazione di pagine Web personalizzate per le API di Web Authentication Broker Windows 8 Web Authentication Broker.</span><span class="sxs-lookup"><span data-stu-id="86bb3-104">This section guides web developers and online providers for creating web pages tailored for the Windows 8 Web Authentication Broker APIs.</span></span> <span data-ttu-id="86bb3-105">Fornisce indicazioni visive e interattive per un'esperienza utente end-to-end della pagina Web e come abilitare le funzionalità single sign-on (SSO).</span><span class="sxs-lookup"><span data-stu-id="86bb3-105">It provides the visual and interactive recommendations for an end-to-end user experience of the web page as well as how to enable single sign-on (SSO) capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="86bb3-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="86bb3-106">In this section</span></span>



| <span data-ttu-id="86bb3-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="86bb3-107">Topic</span></span>                                                                                                     | <span data-ttu-id="86bb3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86bb3-108">Description</span></span>                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86bb3-109">Considerazioni relative allo sviluppo di pagine Web</span><span class="sxs-lookup"><span data-stu-id="86bb3-109">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)<br/> | <span data-ttu-id="86bb3-110">Web Authentication Broker si basa sulle stesse tecnologie che Internet Explorer in Windows.</span><span class="sxs-lookup"><span data-stu-id="86bb3-110">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="86bb3-111">Tuttavia, a causa di uno scopo molto speciale di questo componente, alcune funzionalità del Internet Explorer sono state disabilitate o bloccate in una configurazione specifica.</span><span class="sxs-lookup"><span data-stu-id="86bb3-111">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <br/> |
| [<span data-ttu-id="86bb3-112">Come personalizzare gli elementi dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="86bb3-112">How to customize the UI elements</span></span>](how-to-customize-the-ui-elements.md)<br/>                       | <span data-ttu-id="86bb3-113">Una pagina Web personalizza l'interfaccia utente con il titolo, l'icona e il colore dell'intestazione usando i tag di metadati definiti nella pagina Web.</span><span class="sxs-lookup"><span data-stu-id="86bb3-113">A web page customizes the user interface (UI) with the title, icon, and header color by using metadata tags defined on the web page.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="86bb3-114">Esercitazione per l'autenticazione di pagine Web</span><span class="sxs-lookup"><span data-stu-id="86bb3-114">Tutorial for authenticating web pages</span></span>](tutorial-for-authenticating-web-pages.md)<br/>             |                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="86bb3-115">Problemi relativi all'autenticazione Web</span><span class="sxs-lookup"><span data-stu-id="86bb3-115">Web authentication problems</span></span>](web-authentication-problems.md)<br/>                                 | <span data-ttu-id="86bb3-116">Questo argomento descrive i suggerimenti per la risoluzione dei problemi relativi all'uso delle API di Web Authentication Broker per le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="86bb3-116">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="86bb3-117">Domande frequenti su Web Authentication Broker</span><span class="sxs-lookup"><span data-stu-id="86bb3-117">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.yml)<br/>                     | <span data-ttu-id="86bb3-118">Domande frequenti su Web Authentication Broker.</span><span class="sxs-lookup"><span data-stu-id="86bb3-118">Frequently asked questions for Web Authentication Broker.</span></span><br/>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="86bb3-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86bb3-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="86bb3-120">[Panoramica del broker di autenticazione Web](/previous-versions/windows/apps/hh750287(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="86bb3-120">[Web authentication broker overview](/previous-versions/windows/apps/hh750287(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="86bb3-121">App di esempio di Web Authentication Broker SDK</span><span class="sxs-lookup"><span data-stu-id="86bb3-121">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="86bb3-122">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="86bb3-122">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

