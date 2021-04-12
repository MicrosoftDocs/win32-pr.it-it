---
description: NLS include numerose funzioni API che possono essere usate dalle applicazioni per eseguire il mapping dei dati delle impostazioni locali tra gli identificatori delle impostazioni locali e i nomi delle impostazioni locali ed elencare le impostazioni locali non associate ad alcun paese.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Mapping dei dati delle impostazioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226452"
---
# <a name="mapping-locale-data"></a><span data-ttu-id="48738-103">Mapping dei dati delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="48738-103">Mapping Locale Data</span></span>

<span data-ttu-id="48738-104">NLS include numerose funzioni API che possono essere usate dalle applicazioni per eseguire il mapping dei dati delle impostazioni locali tra gli [identificatori](locale-identifiers.md) delle impostazioni locali e [i nomi delle impostazioni locali](locale-names.md)ed elencare le impostazioni locali non associate ad alcun paese.</span><span class="sxs-lookup"><span data-stu-id="48738-104">NLS includes a number of API functions that your applications can use to map locale data between [locale identifiers](locale-identifiers.md) and [locale names](locale-names.md), and list neutral locales.</span></span> <span data-ttu-id="48738-105">In questo argomento viene illustrato l'utilizzo di queste funzioni in Windows Vista e versioni successive e nei sistemi operativi precedenti a Windows Vista (talvolta denominati "sistemi di livello inferiore").</span><span class="sxs-lookup"><span data-stu-id="48738-105">This topic discusses the use of these functions on Windows Vista and later and on pre-Windows Vista operating systems (sometimes called "downlevel systems").</span></span>

## <a name="map-locale-data-on-windows-vista-and-later"></a><span data-ttu-id="48738-106">Mappare i dati delle impostazioni locali in Windows Vista e versioni successive</span><span class="sxs-lookup"><span data-stu-id="48738-106">Map Locale Data on Windows Vista and Later</span></span>

<span data-ttu-id="48738-107">NLS fornisce diverse funzioni di mapping delle impostazioni locali da utilizzare per le applicazioni sviluppate per l'esecuzione in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="48738-107">NLS provides several locale mapping functions for use by applications that you develop to run on Windows Vista and later.</span></span> <span data-ttu-id="48738-108">Sono incluse anche le funzioni che possono essere utilizzate dalle applicazioni per enumerare le impostazioni locali non associate ad alcun paese.</span><span class="sxs-lookup"><span data-stu-id="48738-108">It also includes functions that your applications can use to enumerate neutral locales.</span></span>

<span data-ttu-id="48738-109">**Usare le funzioni di conversione standard per il mapping dei dati**</span><span class="sxs-lookup"><span data-stu-id="48738-109">**Use the Standard Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="48738-110">Per eseguire il mapping tra un nome delle impostazioni locali e un identificatore delle impostazioni locali, l'applicazione può chiamare la funzione [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) .</span><span class="sxs-lookup"><span data-stu-id="48738-110">To map between a locale name and a locale identifier, your application can call the [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function.</span></span> <span data-ttu-id="48738-111">L'applicazione usa [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) per eseguire il mapping tra un identificatore delle impostazioni locali e un nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="48738-111">The application uses [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to map between a locale identifier and a locale name.</span></span>

<span data-ttu-id="48738-112">**Elenca impostazioni locali non associate ad alcun paese**</span><span class="sxs-lookup"><span data-stu-id="48738-112">**List Neutral Locales**</span></span>

<span data-ttu-id="48738-113">Per enumerare le impostazioni locali non associate ad alcun paese per Windows 7 e versioni successive, l'applicazione può chiamare [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) con *DwFlags* impostato su [**locale \_ NEUTRALDATA**](locale-neutraldata.md).</span><span class="sxs-lookup"><span data-stu-id="48738-113">To enumerate neutral locales for Windows 7 and later, your application can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) with *dwFlags* set to [**LOCALE\_NEUTRALDATA**](locale-neutraldata.md).</span></span> <span data-ttu-id="48738-114">Può anche usare [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCType* impostato su [**impostazioni locali \_ INEUTRAL**](locale-ineutral.md).</span><span class="sxs-lookup"><span data-stu-id="48738-114">It can also use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with *LCType* set to [**LOCALE\_INEUTRAL**](locale-ineutral.md).</span></span>

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="48738-115">Mappare i dati delle impostazioni locali nei sistemi operativi precedenti a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48738-115">Map Locale Data on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="48738-116">NLS include una libreria di collegamento diretto (DLL) da usare per le applicazioni sviluppate per l'esecuzione in sistemi operativi precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="48738-116">NLS includes a direct-link library (DLL) to use for applications that you develop to run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="48738-117">La DLL supporta le funzioni di conversione ed elenco per il mapping dei dati.</span><span class="sxs-lookup"><span data-stu-id="48738-117">The DLL supports both conversion and listing functions for data mapping.</span></span>

> [!Note]  
> <span data-ttu-id="48738-118">Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive non devono utilizzare le funzioni di mapping o elenco di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="48738-118">Applications that only run on Windows Vista and later should not use the downlevel mapping or listing functions.</span></span>

 

<span data-ttu-id="48738-119">**Usare le funzioni di conversione di livello inferiore per il mapping dei dati**</span><span class="sxs-lookup"><span data-stu-id="48738-119">**Use the Downlevel Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="48738-120">L'applicazione destinata a un sistema di livello inferiore può chiamare la funzione [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) per convertire un identificatore delle impostazioni locali in un nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="48738-120">Your application targeted at a downlevel system can call the [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) function to convert a locale identifier to a locale name.</span></span> <span data-ttu-id="48738-121">Se è necessario convertire un nome delle impostazioni locali in un identificatore delle impostazioni locali, deve chiamare [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).</span><span class="sxs-lookup"><span data-stu-id="48738-121">If it needs to convert a locale name to a locale identifier, it should call [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).</span></span>

<span data-ttu-id="48738-122">**Usare le funzioni elenco di livello inferiore per enumerare le impostazioni locali neutre**</span><span class="sxs-lookup"><span data-stu-id="48738-122">**Use the Downlevel Listing Functions to Enumerate Neutral Locales**</span></span>

<span data-ttu-id="48738-123">L'applicazione deve chiamare [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) per recuperare l'identificatore delle impostazioni locali dell'elemento padre per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="48738-123">Your application should call the [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) to retrieve the locale identifier of the parent for a locale.</span></span> <span data-ttu-id="48738-124">Se l'applicazione deve ottenere il nome delle impostazioni locali dell'elemento padre per le impostazioni locali, deve chiamare [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).</span><span class="sxs-lookup"><span data-stu-id="48738-124">If the application needs to get the locale name of the parent for the locale, it should call [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="48738-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48738-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48738-126">Uso del supporto per le lingue nazionali</span><span class="sxs-lookup"><span data-stu-id="48738-126">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="48738-127">Identificatori delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="48738-127">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="48738-128">Nomi delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="48738-128">Locale Names</span></span>](locale-names.md)
</dt> </dl>

 

 



