---
description: Per semplificare l'implementazione del driver quanto più possibile, Windows Image Acquisition (WIA) fornisce una libreria di servizi minidriver che esegue molte delle attività amministrative richieste dall'architettura WIA.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: Libreria di servizi WIA minidriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45856fb795810e4e447a226f1b92a28698f08cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307311"
---
# <a name="wia-minidriver-service-library"></a><span data-ttu-id="017cd-103">Libreria di servizi WIA minidriver</span><span class="sxs-lookup"><span data-stu-id="017cd-103">WIA Minidriver Service Library</span></span>

<span data-ttu-id="017cd-104">Per semplificare l'implementazione del driver quanto più possibile, Windows Image Acquisition (WIA) fornisce una libreria di servizi minidriver che esegue molte delle attività amministrative richieste dall'architettura WIA.</span><span class="sxs-lookup"><span data-stu-id="017cd-104">To simplify driver implementation as much as possible, Windows Image Acquisition (WIA) provides a Minidriver Service Library that performs many of the administrative tasks required by the WIA architecture.</span></span> <span data-ttu-id="017cd-105">La libreria del servizio fornisce funzioni di supporto per la gestione dell'albero del dispositivo degli oggetti dell' [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) .</span><span class="sxs-lookup"><span data-stu-id="017cd-105">The service library provides helper functions to maintain the device's tree of [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) objects.</span></span>

<span data-ttu-id="017cd-106">Le funzioni di base della libreria di servizi eseguono le funzioni di supporto che la maggior parte dei driver di dispositivo avrebbe altrimenti necessario implementare.</span><span class="sxs-lookup"><span data-stu-id="017cd-106">The basic service library functions perform helper functions that most device drivers would otherwise need to implement.</span></span> <span data-ttu-id="017cd-107">Queste funzioni leggono e scrivono le proprietà.</span><span class="sxs-lookup"><span data-stu-id="017cd-107">These functions read and write properties.</span></span> <span data-ttu-id="017cd-108">Creano inoltre oggetti elemento del driver e copia le proprietà delle informazioni sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="017cd-108">They also create driver item objects and copy device information properties.</span></span>

 

 



