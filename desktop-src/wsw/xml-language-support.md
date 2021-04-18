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
# <a name="xml-language-support"></a>Supporto del linguaggio XML

In questa sezione viene descritto il livello di supporto del linguaggio XML in WWS.


Vedere le funzioni DownlevelLCIDToLocaleName nelle versioni di Windows precedenti a Windows Vista e LCIDToLocalName in caso contrario, per eseguire la conversione tra un LCID e un valore XML: lang.

Durante la lettura, è possibile utilizzare [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) per individuare il valore di un attributo "XML: lang" nell'ambito.

Quando si scrive, è possibile usare [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) per scrivere un attributo "XML: lang".

 

 




