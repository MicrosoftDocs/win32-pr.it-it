---
description: Gli elementi Windows Image Acquisition (WIA) 2,0 sono raggruppati in categorie che definiscono la modalità di trattamento o di utilizzo di un IWiaItem2.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: GUID della categoria di elementi WIA 2,0 (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307300"
---
# <a name="wia-20-item-category-guids"></a><span data-ttu-id="53c48-103">GUID categoria elemento WIA 2,0</span><span class="sxs-lookup"><span data-stu-id="53c48-103">WIA 2.0 Item Category GUIDs</span></span>

<span data-ttu-id="53c48-104">Gli elementi Windows Image Acquisition (WIA) 2,0 sono raggruppati in categorie che definiscono la modalità di trattamento o di utilizzo di un [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="53c48-104">Windows Image Acquisition (WIA) 2.0 items are grouped into categories that define how a [**IWiaItem2**](-wia-iwiaitem2.md) is to be treated or used.</span></span> <span data-ttu-id="53c48-105">Se, ad esempio, l'elemento rappresenta un feeder, l'applicazione deve prevedere che contenga le proprietà richieste del feed di documenti e funzioni come un feeder di documenti.</span><span class="sxs-lookup"><span data-stu-id="53c48-105">For example, if the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="53c48-106">Se l'elemento rappresenta un file terminato, un'applicazione WIA 2,0 dovrebbe gestirla in questo modo, supponendo che i dati siano statici e presenti sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53c48-106">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="53c48-107">(Le regole per ogni elemento verranno definite nei singoli documenti delle specifiche). Ogni categoria ha una costante di tipo GUID.</span><span class="sxs-lookup"><span data-stu-id="53c48-107">(The rules for each item will be defined in their individual specification documents.) Each category has a GUID type constant.</span></span>



| <span data-ttu-id="53c48-108">Costante</span><span class="sxs-lookup"><span data-stu-id="53c48-108">Constant</span></span>                                                                                                                                                                                               | <span data-ttu-id="53c48-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53c48-109">Description</span></span>                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <span data-ttu-id="53c48-110"><dt>**\_categoria WIA \_ auto**</dt></span><span class="sxs-lookup"><span data-stu-id="53c48-110"><dt>**WIA\_CATEGORY\_AUTO**</dt></span></span> </dl>                             | <span data-ttu-id="53c48-111">Elemento che rappresenta le impostazioni di configurazione automatica per un dispositivo scanner WIA 2,0 che supporta l'analisi configurata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="53c48-111">An item that represents the automatic configuration settings for a WIA 2.0 scanner device that supports auto-configured scanning.</span></span><br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <span data-ttu-id="53c48-112"><dt>**\_feed di categoria WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53c48-112"><dt>**WIA\_CATEGORY\_FEEDER**</dt></span></span> </dl>                       | <span data-ttu-id="53c48-113">Elemento del feeder che è un'origine dati programmabile e segue le regole standard e i set di proprietà necessari per supportare i feed di documenti.</span><span class="sxs-lookup"><span data-stu-id="53c48-113">A feeder item that is a programmable data source and follows the standard rules and property sets required to support document feeders.</span></span><br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <span data-ttu-id="53c48-114"><dt>**\_feeder di categoria WIA \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53c48-114"><dt>**WIA\_CATEGORY\_FEEDER\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="53c48-115">Origine dati programmabile che descrive l'origine dati di back-side di un elemento del feeder di base duplex.</span><span class="sxs-lookup"><span data-stu-id="53c48-115">A programmable data source describing the back side data source of a duplex base feeder item.</span></span><br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <span data-ttu-id="53c48-116"><dt>**\_ \_ primo feed di categoria \_ WIA**</dt></span><span class="sxs-lookup"><span data-stu-id="53c48-116"><dt>**WIA\_CATEGORY\_FEEDER\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="53c48-117">Origine dati programmabile che descrive l'origine dati del lato anteriore di un elemento del feeder di base duplex.</span><span class="sxs-lookup"><span data-stu-id="53c48-117">A programmable data source describing the front side data source of a duplex base feeder item.</span></span><br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <span data-ttu-id="53c48-118"><dt>**\_film di categoria WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53c48-118"><dt>**WIA\_CATEGORY\_FILM**</dt></span></span> </dl>                             | <span data-ttu-id="53c48-119">Un elemento di film che è un'origine dati programmabile e segue le regole standard e i set di proprietà necessari per supportare le unità di analisi dei film.</span><span class="sxs-lookup"><span data-stu-id="53c48-119">A film item that is a programmable data source and follows the standard rules and property sets required to support film scanning units.</span></span><br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <span data-ttu-id="53c48-120"><dt>**\_file di categoria \_ completato \_ WIA**</dt></span><span class="sxs-lookup"><span data-stu-id="53c48-120"><dt>**WIA\_CATEGORY\_FINISHED\_FILE**</dt></span></span> </dl> | <span data-ttu-id="53c48-121">Un elemento che non è un'origine dati programmabile o un elemento che fornisce dati in un formato di file finito o un elemento cartella che contiene gli elementi del formato di file completati.</span><span class="sxs-lookup"><span data-stu-id="53c48-121">An item that is not a programmable data source, or an item that provides data in a finished file format, or a folder item that contains finished file format items.</span></span><br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <span data-ttu-id="53c48-122"><dt>**\_categoria WIA \_ piana**</dt></span><span class="sxs-lookup"><span data-stu-id="53c48-122"><dt>**WIA\_CATEGORY\_FLATBED**</dt></span></span> </dl>                    | <span data-ttu-id="53c48-123">Un elemento piano che rappresenta un'origine dati programmabile e segue le regole standard e i set di proprietà necessari per supportare l'analisi con piastra piana.</span><span class="sxs-lookup"><span data-stu-id="53c48-123">A flatbed item that is a programmable data source and follows the standard rules and property sets required to support flatbed platen scanning.</span></span><br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <span data-ttu-id="53c48-124"><dt>**\_cartella di categoria WIA \_**</dt></span><span class="sxs-lookup"><span data-stu-id="53c48-124"><dt>**WIA\_CATEGORY\_FOLDER**</dt></span></span> </dl>                       | <span data-ttu-id="53c48-125">Elemento di archiviazione di cartelle (non un'origine dati programmabile) che contiene altri elementi di cartella o file finiti o entrambi.</span><span class="sxs-lookup"><span data-stu-id="53c48-125">A folder storage item (not a programmable data source) containing other folder items or finished files or both.</span></span><br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <span data-ttu-id="53c48-126"><dt>**\_radice categoria \_ WIA**</dt></span><span class="sxs-lookup"><span data-stu-id="53c48-126"><dt>**WIA\_CATEGORY\_ROOT**</dt></span></span> </dl>                             | <span data-ttu-id="53c48-127">Elemento radice per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53c48-127">The root item for the device.</span></span> <br/>                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="53c48-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53c48-128">Requirements</span></span>



| <span data-ttu-id="53c48-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="53c48-129">Requirement</span></span> | <span data-ttu-id="53c48-130">Valore</span><span class="sxs-lookup"><span data-stu-id="53c48-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="53c48-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53c48-131">Minimum supported client</span></span><br/> | <span data-ttu-id="53c48-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53c48-132">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="53c48-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53c48-133">Minimum supported server</span></span><br/> | <span data-ttu-id="53c48-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53c48-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="53c48-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53c48-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="53c48-136"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="53c48-136"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




