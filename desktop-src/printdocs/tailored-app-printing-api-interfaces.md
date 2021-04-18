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
# <a name="print-document-package-api-interfaces"></a>Interfacce API del pacchetto di stampa del documento

Le interfacce seguenti vengono usate da un'app per gestire il pacchetto del documento di stampa.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                       | Descrizione                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDocumentPackageStatusEvent**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | Rappresenta lo stato di avanzamento del processo di stampa.<br/>                                                                                                                                                                        |
| [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | Consente agli utenti di enumerare i tipi di destinazione del pacchetto supportati e di crearne uno con un ID tipo specificato. **IPrintDocumentPackageTarget** supporta inoltre il rilevamento dello stato di avanzamento e dell'annullamento della stampa del pacchetto.<br/> |
| [**IPrintDocumentPackageTargetFactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | Utilizzato con [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) per l'avvio di un processo di stampa.<br/>                                                                                                               |



 

 

