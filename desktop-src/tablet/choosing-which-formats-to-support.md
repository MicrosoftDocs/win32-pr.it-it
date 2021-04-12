---
description: Il tipo di applicazione creato impone il formato di persistenza dell'input penna da supportare.
ms.assetid: bd0a4382-f014-4f03-990d-d2f96aa76ab8
title: Scelta dei formati da supportare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 891fa1c21dd3178e925deab27525afa7fa70fa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233883"
---
# <a name="choosing-which-formats-to-support"></a>Scelta dei formati da supportare

Il tipo di applicazione creato impone il formato di persistenza dell'input penna da supportare.

## <a name="single-ink-object-applications"></a>Applicazioni oggetto a input singolo

Le applicazioni i cui documenti contengono solo input penna devono usare il formato ISF (Ink Serialized Format). Devono essere in grado di copiare e incollare il formato ISF (Ink Serialized Format). Un esempio è costituito da un'applicazione per il disegno o l'annotazione. Queste applicazioni possono usare i metodi [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)e [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste) .

## <a name="complex-applications"></a>Applicazioni complesse

Le applicazioni i cui documenti contengono altro contenuto, ad esempio il testo, devono copiare il codice HTML con i file Graphics Interchange Format (GIF) fortificati, oltre ad ISF. Il codice HTML stesso deve essere generato dall'applicazione, anche se le API (Application Programming Interface) di Tablet PC generano file GIF. Queste applicazioni devono inoltre essere in grado di copiare e incollare l'ISF per l'interoperabilità con le applicazioni descritte in precedenza.

## <a name="rtf"></a>RTF

Un'applicazione deve essere in grado di produrre RTF (Rich Text Format) se è necessaria l'interoperabilità con Microsoft Word 2002 o altre applicazioni legacy.

## <a name="mime-support"></a>Supporto MIME

La tabella seguente elenca le intestazioni MIME (suggested Multipurpose Internet Mail Extensions) e le estensioni di file per l'input penna salvati in modo permanente nei file usando il formato ISF o GIF. Questi valori si trovano nell'enumerazione [**PersistenceFormat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat) .



| Formato di persistenza            | Intestazione MIME                                                                                    | Estensione nome del file            |
|-------------------------------|------------------------------------------------------------------------------------------------|---------------------------|
| **Base64Gif**                 | Content-Type: Application/x-ms-Ink Content-Transfer-Encoding: Base64<br/>                | Non applicabile<br/> |
| **Base64InkSerializedFormat** | Content-Type: Content-Type: image/gif; Format = input penna Content-Transfer-Encoding: Base64<br/> | Non applicabile<br/> |
| **Gif**                       | Content-Type: Application/x-ms-Ink<br/>                                                  | gif<br/>           |
| **InkSerializedFormat**       | Content-Type: Content-Type: image/gif; Format = input penna<br/>                                   | . ISF<br/>           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Enumerazione PersistenceFormat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)
</dt> </dl>

 

 




