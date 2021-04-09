---
description: Panoramica della gestione degli errori quando si usano le API (Application Programming Interface) di StylusInput.
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: Considerazioni sulla gestione degli errori per l'API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fa582a8dbf531588f6d3d0c142c4ec7b40a058
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966732"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a><span data-ttu-id="863d6-103">Considerazioni sulla gestione degli errori per l'API StylusInput</span><span class="sxs-lookup"><span data-stu-id="863d6-103">Error Handling Considerations for the StylusInput API</span></span>

<span data-ttu-id="863d6-104">Le eccezioni non gestite generate da un plug-in vengono rilevate dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="863d6-104">Unhandled exceptions thrown by a plug-in are caught by the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="863d6-105">Quando un plug-in genera un'eccezione, il flusso di dati normale viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="863d6-105">When a plug-in throws an exception, the normal flow of data is interrupted.</span></span> <span data-ttu-id="863d6-106">Oggetto **RealTimeStylus** :</span><span class="sxs-lookup"><span data-stu-id="863d6-106">The **RealTimeStylus** object:</span></span>

1.  <span data-ttu-id="863d6-107">Crea un oggetto [ErrorData](/previous-versions/ms575221(v=vs.100)) (nel codice gestito).</span><span class="sxs-lookup"><span data-stu-id="863d6-107">Creates an [ErrorData](/previous-versions/ms575221(v=vs.100)) object (in managed code).</span></span>
2.  <span data-ttu-id="863d6-108">Chiama il metodo [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) (nel codice gestito, ovvero il metodo [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) ) del plug-in che ha generato l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="863d6-108">Calls the [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method (in managed code, either the [Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method) of the plug-in that threw the exception.</span></span>
3.  <span data-ttu-id="863d6-109">Chiama il metodo [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) degli altri plug-in della raccolta.</span><span class="sxs-lookup"><span data-stu-id="863d6-109">Calls the [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method of the remaining plug-ins in that collection.</span></span>
4.  <span data-ttu-id="863d6-110">Se il plug-in che ha generato l'eccezione è un plug-in sincrono, l'oggetto [ErrorData](/previous-versions/ms575221(v=vs.100)) (in codice gestito) viene aggiunto alla coda di output.</span><span class="sxs-lookup"><span data-stu-id="863d6-110">If the plug-in that threw the exception is a synchronous plug-in, the [ErrorData](/previous-versions/ms575221(v=vs.100)) object (in managed code) is added to the output queue.</span></span>
5.  <span data-ttu-id="863d6-111">L'oggetto [**RealTimeStylus**](realtimestylus-class.md) riprende la normale elaborazione dei dati originali.</span><span class="sxs-lookup"><span data-stu-id="863d6-111">The [**RealTimeStylus**](realtimestylus-class.md) object resumes normal processing of the original data.</span></span>

<span data-ttu-id="863d6-112">Se un plug-in genera un'eccezione dal relativo metodo [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) , l'oggetto [**RealTimeStylus**](realtimestylus-class.md) intercetta l'eccezione, ma non genera un nuovo oggetto [ErrorData](/previous-versions/ms575221(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="863d6-112">If a plug-in throws an exception from its [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method, the [**RealTimeStylus**](realtimestylus-class.md) object catches the exception but does not generate a new [ErrorData](/previous-versions/ms575221(v=vs.100)) object.</span></span> <span data-ttu-id="863d6-113">Per ulteriori informazioni sulla modalità di aggiunta di ErrorData alla coda, vedere [dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).</span><span class="sxs-lookup"><span data-stu-id="863d6-113">For more information about how ErrorData is added to the queue, see [Plug-in Data and the RealTimeStylus Class](plug-in-data-and-the-realtimestylus-class.md).</span></span>

<span data-ttu-id="863d6-114">L'oggetto [**RealTimeStylus**](realtimestylus-class.md) non interrompe l'elaborazione dei dati dal flusso di dati della penna del tablet quando uno dei relativi plug-in genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="863d6-114">The [**RealTimeStylus**](realtimestylus-class.md) object does not stop processing data from the tablet pen's data stream when one of its plug-ins throws an exception.</span></span> <span data-ttu-id="863d6-115">A seconda della progettazione, è possibile che alcuni plug-in debbano sottoscrivere la notifica [ErrorData](/previous-versions/ms575221(v=vs.100)) e modificarne il comportamento quando si verifica un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="863d6-115">Depending on your design, some of your plug-ins may need to subscribe to the [ErrorData](/previous-versions/ms575221(v=vs.100)) notification and modify their behavior when an exception occurs.</span></span>

 

 
