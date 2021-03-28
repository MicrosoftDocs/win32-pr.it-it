---
description: Funzioni di notifica
ms.assetid: 44f69e05-1f08-48da-abb7-7e0a96c0cd26
title: Funzioni di notifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e5ca0bbcd9f2f184abd312fe15d4923e5cf14b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131334"
---
# <a name="notification-functions"></a>Funzioni di notifica



| Flat-funzione                                                                  | Wrapper (metodo)                            | Commenti                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdiplusNotificationHook (OUT ULONG \_ ptr \* token)<br/> | Non viene chiamato dai metodi wrapper.<br/> | La funzione [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) restituisce nel parametro di output un puntatore a una struttura [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) . Uno dei membri della struttura è un puntatore a una funzione hook di notifica con la stessa firma di GdiplusNotificationHook.<br/> Esistono due modi per chiamare la funzione di hook di notifica. è possibile usare il puntatore restituito da [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) oppure è possibile chiamare GdiplusNotificationHook. In realtà, GdiplusNotificationHook verifica semplicemente di avere eliminato il thread in background e quindi chiama la funzione hook di notifica restituita da **GdiplusStartup**.<br/> Il parametro token riceve un identificatore che deve essere passato in un secondo momento a una chiamata corrispondente alla funzione unhook di notifica.<br/>                                                                                                                                         |
| VOID WINGDIPAPI GdiplusNotificationUnhook ( \_ token PTR ulong)<br/>         | Non viene chiamato dai metodi wrapper.<br/> | La funzione [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) restituisce nel parametro di output un puntatore a una struttura [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) . Uno dei membri della struttura è un puntatore a una funzione unhook di notifica con la stessa firma di GdiplusNotificationUnhook.<br/> Esistono due modi per chiamare la funzione di dishook della notifica. è possibile usare il puntatore restituito da [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) oppure è possibile chiamare GdiplusNotificationUnhook. In realtà, GdiplusNotificationUnhook verifica semplicemente di avere eliminato il thread in background e quindi chiama la funzione unhook di notifica restituita da **GdiplusStartup**.<br/> Quando si chiama la funzione unhook di notifica, passare il token ricevuto in precedenza da una chiamata corrispondente alla funzione hook di notifica. Se non si esegue questa operazione, si verificano perdite di risorse che non verranno pulite fino alla chiusura del processo.<br/> |



 

 

 




