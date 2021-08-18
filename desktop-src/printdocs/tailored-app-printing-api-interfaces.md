---
description: Le interfacce seguenti vengono usate da un'app per gestire il pacchetto del documento di stampa.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Interfacce API per la stampa di pacchetti di documenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc37fa31cbda1be6927cbb24bf4b5707d10d9f2d74ed152ef630a2ad6ed588c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470123"
---
# <a name="print-document-package-api-interfaces"></a>Interfacce API per la stampa di pacchetti di documenti

Le interfacce seguenti vengono usate da un'app per gestire il pacchetto del documento di stampa.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                       | Descrizione                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDocumentPackageStatusEvent**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | Rappresenta lo stato del processo di stampa.<br/>                                                                                                                                                                        |
| [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | Consente agli utenti di enumerare i tipi di destinazione del pacchetto supportati e di crearne uno con un ID tipo specificato. **IPrintDocumentPackageTarget** supporta anche il rilevamento dello stato di stampa e dell'annullamento del pacchetto.<br/> |
| [**IPrintDocumentPackageTargetFactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | Usato con [IPrintDocumentPackageTarget per](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) avviare un processo di stampa.<br/>                                                                                                               |



 

 

