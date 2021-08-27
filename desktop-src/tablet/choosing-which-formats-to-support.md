---
description: Il tipo di applicazione creato determina il formato di persistenza dell'input penna da supportare.
ms.assetid: bd0a4382-f014-4f03-990d-d2f96aa76ab8
title: Scelta dei formati da supportare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b8b2197c37db603388a4191e08114800aaba37ee8e89803c7ddfb08be18d3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111001"
---
# <a name="choosing-which-formats-to-support"></a>Scelta dei formati da supportare

Il tipo di applicazione creato determina il formato di persistenza dell'input penna da supportare.

## <a name="single-ink-object-applications"></a>Applicazioni a oggetto input penna singolo

Le applicazioni i cui documenti contengono solo input penna devono usare il formato ISF (Ink Serialized Format). Devono essere in grado di copiare e incollare Ink Serialized Format (ISF). Un esempio è un'applicazione per il disegno o l'annotazione. Queste applicazioni possono usare i [**metodi ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)e [**ClipboardPaste.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)

## <a name="complex-applications"></a>Applicazioni complesse

Le applicazioni i cui documenti contengono altro contenuto, ad esempio testo, devono copiare html con file GRAPHICS INTERCHANGE FORMAT (GIF) fortificati, oltre a ISF. Il codice HTML stesso deve essere generato dall'applicazione, anche se le API (Application Programming Interface) di Tablet PC generano file GIF. Queste applicazioni devono anche essere in grado di copiare e incollare ISF per l'interoperabilità con le applicazioni descritte in precedenza.

## <a name="rtf"></a>RTF

Un'applicazione deve essere in grado di produrre rich text format (RTF) se è necessaria l'interoperabilità con Microsoft Word 2002 o altre applicazioni legacy.

## <a name="mime-support"></a>Supporto MIME

Nella tabella seguente sono elencate le intestazioni Multipurpose Internet Mail Extensions (MIME) suggerite e le estensioni di file per l'input penna che vengono rese persistenti nei file tramite ISF o GIF. Questi valori si trovano [**nell'enumerazione PersistenceFormat.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)



| Formato di persistenza            | Intestazione MIME                                                                                    | Estensione nome del file            |
|-------------------------------|------------------------------------------------------------------------------------------------|---------------------------|
| **Base64Gif**                 | Content-Type: application/x-ms-ink Content-Transfer-Encoding: base64<br/>                | Non applicabile<br/> |
| **Base64InkSerializedFormat** | Content-Type: Content-Type: image/gif; format=ink Content-Transfer-Encoding: base64<br/> | Non applicabile<br/> |
| **Gif**                       | Content-Type: application/x-ms-ink<br/>                                                  | gif<br/>           |
| **InkSerializedFormat**       | Content-Type: Content-Type: image/gif; format=ink<br/>                                   | .isf<br/>           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Enumerazione PersistenceFormat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)
</dt> </dl>

 

 




