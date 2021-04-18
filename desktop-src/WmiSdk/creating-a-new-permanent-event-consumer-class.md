---
description: Uno dei primi passaggi per la creazione di un consumer di eventi permanenti consiste nel creare la classe WMI che descrive il consumer di eventi. In particolare, la classe consumer di eventi permanenti definisce i parametri dell'azione implementata dal consumer fisico.
ms.assetid: a5b6d0b9-8df1-47e3-bb3b-cc69db6d9c0e
ms.tgt_platform: multiple
title: Creazione di una nuova classe di consumer di eventi permanenti
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f8ae8e1e83abcf3b340398d45aefde4c7141e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310390"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a>Creazione di una nuova classe di consumer di eventi permanenti

Uno dei primi passaggi per la creazione di un consumer di eventi permanenti consiste nel creare la classe WMI che descrive il consumer di eventi. In particolare, la classe consumer di eventi permanenti definisce i parametri dell'azione implementata dal consumer fisico.

Nella procedura seguente viene descritto come creare una classe di consumer di eventi permanenti.

**Per creare una classe di consumer di eventi permanenti**

1.  Derivare una classe dalla classe di sistema [**\_ \_ EventConsumer**](--eventconsumer.md) .
2.  Implementare tutti i parametri necessari per elaborare una notifica degli eventi.

Nell'esempio seguente viene illustrata la sintassi utilizzata per creare la classe SMTPConsumerEvent. È possibile usarlo come esempio per creare la nuova classe. La classe [**SMTPEventConsumer**](smtpeventconsumer.md) Invia un messaggio di posta elettronica utilizzando Simple Mail Transfer Protocol (SMTP) ogni volta che viene recapitato un evento. Questa classe è definita in smtpcons. mof.

``` syntax
class SMTPEventConsumer : __EventConsumer
{
  [key] string Name;
  [not_null] string SMTPServer;
  [Template] string Subject;
  [Template] string FromLine;
  [Template] string ReplyToLine;
  [Template] string Message;
  [Template] string ToLine;
  [Template] string CcLine;
  [Template] string BccLine;
  string HeaderFields[];
};
```

Si dovrebbe essere in grado di creare istanze della classe del consumer di eventi permanenti per descrivere uno o più modi per inviare eventi al consumer fisico. Per ulteriori informazioni, vedere [creazione di un consumer logico](creating-a-logical-consumer.md).

 

 



