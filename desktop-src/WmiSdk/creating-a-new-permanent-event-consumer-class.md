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
# <a name="creating-a-new-permanent-event-consumer-class"></a><span data-ttu-id="dffb5-104">Creazione di una nuova classe di consumer di eventi permanenti</span><span class="sxs-lookup"><span data-stu-id="dffb5-104">Creating a New Permanent Event Consumer Class</span></span>

<span data-ttu-id="dffb5-105">Uno dei primi passaggi per la creazione di un consumer di eventi permanenti consiste nel creare la classe WMI che descrive il consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="dffb5-105">One of the first steps in creating a permanent event consumer is to create the WMI class that describes the event consumer.</span></span> <span data-ttu-id="dffb5-106">In particolare, la classe consumer di eventi permanenti definisce i parametri dell'azione implementata dal consumer fisico.</span><span class="sxs-lookup"><span data-stu-id="dffb5-106">Specifically, the permanent event consumer class defines the parameters of the action implemented by the physical consumer.</span></span>

<span data-ttu-id="dffb5-107">Nella procedura seguente viene descritto come creare una classe di consumer di eventi permanenti.</span><span class="sxs-lookup"><span data-stu-id="dffb5-107">The following procedure describes how to create a permanent event consumer class.</span></span>

<span data-ttu-id="dffb5-108">**Per creare una classe di consumer di eventi permanenti**</span><span class="sxs-lookup"><span data-stu-id="dffb5-108">**To create a permanent event consumer class**</span></span>

1.  <span data-ttu-id="dffb5-109">Derivare una classe dalla classe di sistema [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="dffb5-109">Derive a class from the [**\_\_EventConsumer**](--eventconsumer.md) system class.</span></span>
2.  <span data-ttu-id="dffb5-110">Implementare tutti i parametri necessari per elaborare una notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="dffb5-110">Implement any parameters necessary to process an event notification.</span></span>

<span data-ttu-id="dffb5-111">Nell'esempio seguente viene illustrata la sintassi utilizzata per creare la classe SMTPConsumerEvent.</span><span class="sxs-lookup"><span data-stu-id="dffb5-111">The following example shows the syntax used to create the SMTPConsumerEvent class.</span></span> <span data-ttu-id="dffb5-112">È possibile usarlo come esempio per creare la nuova classe.</span><span class="sxs-lookup"><span data-stu-id="dffb5-112">You can use this as an example for creating your new class.</span></span> <span data-ttu-id="dffb5-113">La classe [**SMTPEventConsumer**](smtpeventconsumer.md) Invia un messaggio di posta elettronica utilizzando Simple Mail Transfer Protocol (SMTP) ogni volta che viene recapitato un evento.</span><span class="sxs-lookup"><span data-stu-id="dffb5-113">The [**SMTPEventConsumer**](smtpeventconsumer.md) class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="dffb5-114">Questa classe è definita in smtpcons. mof.</span><span class="sxs-lookup"><span data-stu-id="dffb5-114">This class is defined in smtpcons.mof.</span></span>

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

<span data-ttu-id="dffb5-115">Si dovrebbe essere in grado di creare istanze della classe del consumer di eventi permanenti per descrivere uno o più modi per inviare eventi al consumer fisico.</span><span class="sxs-lookup"><span data-stu-id="dffb5-115">You should be able to create instances of your permanent event consumer class to describe one or more ways to send events to your physical consumer.</span></span> <span data-ttu-id="dffb5-116">Per ulteriori informazioni, vedere [creazione di un consumer logico](creating-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="dffb5-116">For more information, see [Creating a Logical Consumer](creating-a-logical-consumer.md).</span></span>

 

 



