---
title: Uso dell'estensione ADSI per la configurazione di Servizi Desktop remoto utente
description: L'amministrazione delle proprietà utente specifiche di Servizi Desktop remoto è possibile utilizzando i metodi implementati dall'estensione ADSI (Active Directory Service Interfaces), assemblata con la libreria a collegamento dinamico Tsuserex.dll.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto utilizzando l'estensione ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f115fecf1cce5c518e93206402f76e077109611
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963388"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a><span data-ttu-id="9f249-104">Uso dell'estensione ADSI per la configurazione di Servizi Desktop remoto utente</span><span class="sxs-lookup"><span data-stu-id="9f249-104">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>

<span data-ttu-id="9f249-105">L'estensione ADSI (Active Directory Service Interfaces) per la configurazione dell'utente Servizi Desktop remoto è una raccolta di pacchetti con la libreria a collegamento dinamico Tsuserex.dll.</span><span class="sxs-lookup"><span data-stu-id="9f249-105">The Active Directory Service Interfaces (ADSI) extension for Remote Desktop Services user configuration is a library that is packaged with the dynamic-link library Tsuserex.dll.</span></span> <span data-ttu-id="9f249-106">L'amministrazione delle proprietà utente specifiche di Servizi Desktop remoto è possibile utilizzando i metodi implementati dall'estensione.</span><span class="sxs-lookup"><span data-stu-id="9f249-106">Administration of Remote Desktop Services-specific user properties is possible using the methods implemented by the extension.</span></span> <span data-ttu-id="9f249-107">I metodi consentono la configurazione delle proprietà disponibili nell'interfaccia di estensione per Servizi Desktop remoto utenti.</span><span class="sxs-lookup"><span data-stu-id="9f249-107">The methods allow configuration of the properties that are available in the extension interface for Remote Desktop Services users.</span></span>

<span data-ttu-id="9f249-108">L'estensione ADSI per Servizi Desktop remoto Configurazione utente supporta l'analisi e la manipolazione delle proprietà Servizi Desktop remoto utente archiviate nel database del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="9f249-108">The ADSI extension for Remote Desktop Services user configuration supports the examination and manipulation of Remote Desktop Services user properties stored in the Directory Service database.</span></span> <span data-ttu-id="9f249-109">L'estensione supporta inoltre la configurazione di proprietà utente archiviate nel Active Directory tramite l'API LDAP (Lightweight Directory Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="9f249-109">The extension also supports configuration of user properties that are stored in the Active Directory, through the Lightweight Directory Access Protocol (LDAP) API.</span></span>

<span data-ttu-id="9f249-110">Il provider implementa i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f249-110">The provider implements the following methods:</span></span>

-   <span data-ttu-id="9f249-111">[**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get).</span><span class="sxs-lookup"><span data-stu-id="9f249-111">[**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get).</span></span> <span data-ttu-id="9f249-112">Questo metodo cerca una proprietà o un set di proprietà specifico in un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="9f249-112">This method searches for a specific property or set of properties on an instance of the class.</span></span>
-   <span data-ttu-id="9f249-113">[**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put).</span><span class="sxs-lookup"><span data-stu-id="9f249-113">[**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put).</span></span> <span data-ttu-id="9f249-114">Questo metodo configura una proprietà o un set di proprietà specifico in un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="9f249-114">This method configures a specific property or set of properties on an instance of the class.</span></span>

<span data-ttu-id="9f249-115">Per un elenco delle proprietà utente Servizi Desktop remoto specifiche che è possibile configurare, vedere la Guida di [riferimento per l'estensione ADSI per Servizi Desktop remoto Configurazione utente](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="9f249-115">See the [Reference for the ADSI Extension for Remote Desktop Services User Configuration](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) for a list of the specific Remote Desktop Services user properties you can configure.</span></span>

<span data-ttu-id="9f249-116">Per ulteriori informazioni sull'accesso e la modifica degli attributi con ADSI, vedere [accesso e modifica di dati con ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span><span class="sxs-lookup"><span data-stu-id="9f249-116">For more information about accessing and modifying attributes with ADSI, see [Accessing and Manipulating Data with ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span></span>

<span data-ttu-id="9f249-117">Per ulteriori informazioni sull'utilizzo delle convenzioni di denominazione ADSI e delle stringhe AdsPath, vedere le informazioni sui singoli [provider di servizi ADSI](/windows/desktop/ADSI/adsi-system-providers) nella documentazione di [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform SDK (SDK).</span><span class="sxs-lookup"><span data-stu-id="9f249-117">For more information about using ADSI naming conventions and AdsPath strings, see the information about individual [ADSI Service Providers](/windows/desktop/ADSI/adsi-system-providers) in the [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform Software Development Kit (SDK) documentation.</span></span>

 

 