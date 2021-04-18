---
title: Supporto del linguaggio XML
description: In questa sezione viene descritto il livello di supporto del linguaggio XML in WWS.
ms.assetid: c3408c2a-6506-4a2e-8083-b4a0154a6918
keywords:
- Servizi Web per il supporto del linguaggio XML per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13425d2ed9c878c3a63dd5b5908ffbab4f2f177
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300700"
---
# <a name="xml-language-support"></a><span data-ttu-id="0be81-106">Supporto del linguaggio XML</span><span class="sxs-lookup"><span data-stu-id="0be81-106">XML Language Support</span></span>

<span data-ttu-id="0be81-107">In questa sezione viene descritto il livello di supporto del linguaggio XML in WWS.</span><span class="sxs-lookup"><span data-stu-id="0be81-107">This section describe level of XML Language support in WWS.</span></span>


<span data-ttu-id="0be81-108">Vedere le funzioni DownlevelLCIDToLocaleName nelle versioni di Windows precedenti a Windows Vista e LCIDToLocalName in caso contrario, per eseguire la conversione tra un LCID e un valore XML: lang.</span><span class="sxs-lookup"><span data-stu-id="0be81-108">See the functions DownlevelLCIDToLocaleName on versions of Windows earlier than Windows Vista, and LCIDToLocalName otherwise, to convert between an LCID and an xml:lang value.</span></span>

<span data-ttu-id="0be81-109">Durante la lettura, è possibile utilizzare [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) per individuare il valore di un attributo "XML: lang" nell'ambito.</span><span class="sxs-lookup"><span data-stu-id="0be81-109">When reading, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) may be used to discover the value of an "xml:lang" attribute in scope.</span></span>

<span data-ttu-id="0be81-110">Quando si scrive, è possibile usare [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) per scrivere un attributo "XML: lang".</span><span class="sxs-lookup"><span data-stu-id="0be81-110">When writing, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) may be used to write an "xml:lang" attribute.</span></span>

 

 




