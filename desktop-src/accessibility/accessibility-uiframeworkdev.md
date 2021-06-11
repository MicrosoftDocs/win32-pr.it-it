---
description: Informazioni sullo sviluppo di framework dell'interfaccia utente accessibili per Windows con questa panoramica delle funzionalità di accessibilità di Windows che è possibile incorporare nel framework dell'interfaccia utente.
title: Sviluppo di framework dell'interfaccia utente accessibili per Windows
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: d18881913b2a366f086e45473e0f67e57ead66a2
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988846"
---
# <a name="developing-accessible-ui-frameworks-for-windows"></a><span data-ttu-id="62fe1-103">Sviluppo di framework dell'interfaccia utente accessibili per Windows</span><span class="sxs-lookup"><span data-stu-id="62fe1-103">Developing accessible UI frameworks for Windows</span></span>

<span data-ttu-id="62fe1-104">Per essere utilizzabili dal maggior numero possibile di utenti, i framework dell'interfaccia utente creati per la piattaforma Windows devono supportare le funzionalità di accessibilità che semplificano l'uso corretto dei dispositivi Windows da parte di utenti con disabilità, preferenze personali o stili di lavoro specifici.</span><span class="sxs-lookup"><span data-stu-id="62fe1-104">To be usable by as many people as possible, UI frameworks built for the Windows platform should support accessibility features that make it easier for those with disabilities, personal preferences, or specific work styles to use their Windows devices successfully.</span></span>

<span data-ttu-id="62fe1-105">Questa panoramica descrive come compilare un framework dell'interfaccia utente che supporta funzionalità come l'accesso e l'automazione a livello di codice, la navigazione tramite tastiera e i comandi, le opzioni relative a colori e temi e la personalizzazione tramite le impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="62fe1-105">This overview describes how to build a UI framework that supports features such as programmatic access and automation, keyboard navigation and commanding, color and theme options, and personalization through user settings.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="62fe1-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="62fe1-106">In this section</span></span>

- [<span data-ttu-id="62fe1-107">Automazione interfaccia utente per Win32</span><span class="sxs-lookup"><span data-stu-id="62fe1-107">UI Automation for Win32</span></span>](/windows/desktop/winauto/entry-uiauto-win32)
- [<span data-ttu-id="62fe1-108">Accessibilità tramite tastiera</span><span class="sxs-lookup"><span data-stu-id="62fe1-108">Keyboard accessibility</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
- [<span data-ttu-id="62fe1-109">Rispetto delle Contrasto elevato</span><span class="sxs-lookup"><span data-stu-id="62fe1-109">Respecting High Contrast</span></span>](/windows/desktop/w8cookbook/high-contrast-mode)
- [<span data-ttu-id="62fe1-110">Impostazioni utente</span><span class="sxs-lookup"><span data-stu-id="62fe1-110">User settings</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
- [<span data-ttu-id="62fe1-111">Post di blog delle impostazioni utente</span><span class="sxs-lookup"><span data-stu-id="62fe1-111">User settings blog post</span></span>](https://devblogs.microsoft.com/oldnewthing/?p=36243)

<span data-ttu-id="62fe1-112">Esempi</span><span class="sxs-lookup"><span data-stu-id="62fe1-112">Samples</span></span>

- [<span data-ttu-id="62fe1-113">Automazione interfaccia utente'implementazione del framework WPF</span><span class="sxs-lookup"><span data-stu-id="62fe1-113">UI Automation WPF Framework Implementation sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Accessibility)
- <span data-ttu-id="62fe1-114">[Contrasto dell'interfaccia utente ed esempio di impostazioni](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/UI%20contrast%20and%20settings%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="62fe1-114">[UI contrast and settings sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/UI%20contrast%20and%20settings%20sample%20(Windows%208))</span></span>
