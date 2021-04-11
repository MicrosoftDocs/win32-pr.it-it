---
description: Panoramica delle funzionalità di accessibilità di Windows che è possibile incorporare nel Framework dell'interfaccia utente.
title: Sviluppo di framework dell'interfaccia utente accessibili per Windows
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 9083bdb8b9c7ab9dd7dd30c675a72fafa4c065c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127579"
---
# <a name="developing-accessible-ui-frameworks-for-windows"></a><span data-ttu-id="bdda8-103">Sviluppo di framework dell'interfaccia utente accessibili per Windows</span><span class="sxs-lookup"><span data-stu-id="bdda8-103">Developing accessible UI frameworks for Windows</span></span>

<span data-ttu-id="bdda8-104">Per poter essere usato dal numero di persone possibile, i Framework dell'interfaccia utente compilati per la piattaforma Windows dovrebbero supportare le funzionalità di accessibilità che rendono più semplice per gli utenti disabili, le preferenze personali o gli stili di lavoro specifici l'uso corretto dei propri dispositivi Windows.</span><span class="sxs-lookup"><span data-stu-id="bdda8-104">To be usable by as many people as possible, UI frameworks built for the Windows platform should support accessibility features that make it easier for those with disabilities, personal preferences, or specific work styles to use their Windows devices successfully.</span></span>

<span data-ttu-id="bdda8-105">Questa panoramica descrive come creare un Framework dell'interfaccia utente che supporta funzionalità quali l'accesso a livello di codice e l'automazione, la navigazione da tastiera e i comandi, le opzioni relative ai colori e ai temi e la personalizzazione tramite le impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="bdda8-105">This overview describes how to build a UI framework that supports features such as programmatic access and automation, keyboard navigation and commanding, color and theme options, and personalization through user settings.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bdda8-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="bdda8-106">In this section</span></span>

- [<span data-ttu-id="bdda8-107">Automazione interfaccia utente per Win32</span><span class="sxs-lookup"><span data-stu-id="bdda8-107">UI Automation for Win32</span></span>](/windows/desktop/winauto/entry-uiauto-win32)
- [<span data-ttu-id="bdda8-108">Accessibilità tramite tastiera</span><span class="sxs-lookup"><span data-stu-id="bdda8-108">Keyboard accessibility</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
- [<span data-ttu-id="bdda8-109">Rispetto Contrasto elevato</span><span class="sxs-lookup"><span data-stu-id="bdda8-109">Respecting High Contrast</span></span>](/windows/desktop/w8cookbook/high-contrast-mode)
- [<span data-ttu-id="bdda8-110">Impostazioni utente</span><span class="sxs-lookup"><span data-stu-id="bdda8-110">User settings</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
- [<span data-ttu-id="bdda8-111">Post di Blog sulle impostazioni utente</span><span class="sxs-lookup"><span data-stu-id="bdda8-111">User settings blog post</span></span>](https://devblogs.microsoft.com/oldnewthing/?p=36243)

<span data-ttu-id="bdda8-112">Esempi</span><span class="sxs-lookup"><span data-stu-id="bdda8-112">Samples</span></span>

- [<span data-ttu-id="bdda8-113">Esempio di implementazione del framework WPF di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="bdda8-113">UI Automation WPF Framework Implementation sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Accessibility)
- <span data-ttu-id="bdda8-114">[Contrasto dell'interfaccia utente ed esempio di impostazioni](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/UI%20contrast%20and%20settings%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="bdda8-114">[UI contrast and settings sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/UI%20contrast%20and%20settings%20sample%20(Windows%208))</span></span>
