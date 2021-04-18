---
description: Le interfacce seguenti vengono usate da un'app per gestire il pacchetto del documento di stampa.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Interfacce API del pacchetto di stampa del documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc495be5c58598d00250568ff852cf4f897e0b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317288"
---
# <a name="print-document-package-api-interfaces"></a><span data-ttu-id="430a2-103">Interfacce API del pacchetto di stampa del documento</span><span class="sxs-lookup"><span data-stu-id="430a2-103">Print Document Package API Interfaces</span></span>

<span data-ttu-id="430a2-104">Le interfacce seguenti vengono usate da un'app per gestire il pacchetto del documento di stampa.</span><span class="sxs-lookup"><span data-stu-id="430a2-104">The following interfaces are used by an app to manage the print document package.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="430a2-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="430a2-105">In this section</span></span>



| <span data-ttu-id="430a2-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="430a2-106">Topic</span></span>                                                                                       | <span data-ttu-id="430a2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="430a2-107">Description</span></span>                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="430a2-108">**IPrintDocumentPackageStatusEvent**</span><span class="sxs-lookup"><span data-stu-id="430a2-108">**IPrintDocumentPackageStatusEvent**</span></span>](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | <span data-ttu-id="430a2-109">Rappresenta lo stato di avanzamento del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="430a2-109">Represents the progress of the print job.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="430a2-110">**IPrintDocumentPackageTarget**</span><span class="sxs-lookup"><span data-stu-id="430a2-110">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | <span data-ttu-id="430a2-111">Consente agli utenti di enumerare i tipi di destinazione del pacchetto supportati e di crearne uno con un ID tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="430a2-111">Allows users to enumerate the supported package target types and to create one with a given type ID.</span></span> <span data-ttu-id="430a2-112">**IPrintDocumentPackageTarget** supporta inoltre il rilevamento dello stato di avanzamento e dell'annullamento della stampa del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="430a2-112">**IPrintDocumentPackageTarget** also supports the tracking of the package printing progress and cancelling.</span></span><br/> |
| [<span data-ttu-id="430a2-113">**IPrintDocumentPackageTargetFactory**</span><span class="sxs-lookup"><span data-stu-id="430a2-113">**IPrintDocumentPackageTargetFactory**</span></span>](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | <span data-ttu-id="430a2-114">Utilizzato con [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) per l'avvio di un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="430a2-114">Used with [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for starting a print job.</span></span><br/>                                                                                                               |



 

 

