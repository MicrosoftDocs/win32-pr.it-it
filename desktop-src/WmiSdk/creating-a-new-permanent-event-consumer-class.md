---
description: Uno dei primi passaggi per la creazione di un consumer di eventi permanente è la creazione della classe WMI che descrive il consumer di eventi. In particolare, la classe consumer di eventi permanente definisce i parametri dell'azione implementata dal consumer fisico.
ms.assetid: a5b6d0b9-8df1-47e3-bb3b-cc69db6d9c0e
ms.tgt_platform: multiple
title: Creazione di una nuova classe consumer di eventi permanente
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f86f9e8ea4339eb76bdc77087780fcfa9be09f47c92a154c5f89109d90337b41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464281"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a>Creazione di una nuova classe consumer di eventi permanente

Uno dei primi passaggi per la creazione di un consumer di eventi permanente è la creazione della classe WMI che descrive il consumer di eventi. In particolare, la classe consumer di eventi permanente definisce i parametri dell'azione implementata dal consumer fisico.

Nella procedura seguente viene descritto come creare una classe consumer di eventi permanente.

**Per creare una classe consumer di eventi permanente**

1.  Derivare una classe dalla classe di sistema [**\_ \_ EventConsumer.**](--eventconsumer.md)
2.  Implementare tutti i parametri necessari per elaborare una notifica degli eventi.

Nell'esempio seguente viene illustrata la sintassi usata per creare la classe SMTPConsumerEvent. È possibile usarlo come esempio per creare la nuova classe. La [**classe SMTPEventConsumer**](smtpeventconsumer.md) invia un messaggio di posta elettronica usando Simple Mail Transfer Protocol (SMTP) ogni volta che viene recapitato un evento. Questa classe è definita in smtpcons.mof.

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

Dovrebbe essere possibile creare istanze della classe consumer di eventi permanente per descrivere uno o più modi per inviare eventi al consumer fisico. Per altre informazioni, vedere [Creazione di un consumer logico.](creating-a-logical-consumer.md)

 

 



