---
title: Verifica dei valori restituiti di IAccessible
description: Gli sviluppatori client non devono basarsi sulle macro Component Object Model (COM) riuscite ed è Impossibile testare i valori restituiti di IAccessible, perché i valori diversi da S \_ OK sono considerati riusciti.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300184"
---
# <a name="checking-iaccessible-return-values"></a><span data-ttu-id="8d0ff-103">Verifica dei valori restituiti di IAccessible</span><span class="sxs-lookup"><span data-stu-id="8d0ff-103">Checking IAccessible Return Values</span></span>

<span data-ttu-id="8d0ff-104">Gli sviluppatori client non devono basarsi sulle macro Component Object Model (COM) [**riuscite**](/windows/desktop/api/winerror/nf-winerror-succeeded) ed [**è Impossibile**](/windows/desktop/api/winerror/nf-winerror-failed) testare i valori restituiti di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , perché i valori diversi da S \_ OK sono considerati riusciti.</span><span class="sxs-lookup"><span data-stu-id="8d0ff-104">Client developers should not rely on the Component Object Model (COM) macros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) to test [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) return values, because values other than S\_OK are considered a success.</span></span> <span data-ttu-id="8d0ff-105">Ad esempio, un metodo può restituire S \_ false, considerato un esito positivo della macro **succeeded** , ma riceve ancora un puntatore **null** in un parametro di output.</span><span class="sxs-lookup"><span data-stu-id="8d0ff-105">For example, a method can return S\_FALSE, which is considered a success by the **SUCCEEDED** macro, but still receive a **NULL** pointer in an output parameter.</span></span>

<span data-ttu-id="8d0ff-106">Gli sviluppatori client devono evitare la possibilità che alcuni server restituiscano codici di errore diversi dai valori documentati.</span><span class="sxs-lookup"><span data-stu-id="8d0ff-106">Client developers must guard against the possibility that some servers return error codes other than the documented values.</span></span> <span data-ttu-id="8d0ff-107">Per essere sicuri, è necessario assicurarsi che tutti i parametri di output contengano informazioni valide e soddisfino i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="8d0ff-107">To be safe, you must ensure that all the output parameters contain valid information and meet the following criteria:</span></span>

-   <span data-ttu-id="8d0ff-108">Tutti i puntatori sono non **null**.</span><span class="sxs-lookup"><span data-stu-id="8d0ff-108">All pointers are non-**NULL**.</span></span>
-   <span data-ttu-id="8d0ff-109">Il membro **VT** di qualsiasi struttura [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) non è uguale a VT \_ vuoto.</span><span class="sxs-lookup"><span data-stu-id="8d0ff-109">The **vt** member of any [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) structure is not equal to VT\_EMPTY.</span></span>

 

 