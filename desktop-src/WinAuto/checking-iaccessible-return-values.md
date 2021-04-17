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
# <a name="checking-iaccessible-return-values"></a>Verifica dei valori restituiti di IAccessible

Gli sviluppatori client non devono basarsi sulle macro Component Object Model (COM) [**riuscite**](/windows/desktop/api/winerror/nf-winerror-succeeded) ed [**è Impossibile**](/windows/desktop/api/winerror/nf-winerror-failed) testare i valori restituiti di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , perché i valori diversi da S \_ OK sono considerati riusciti. Ad esempio, un metodo può restituire S \_ false, considerato un esito positivo della macro **succeeded** , ma riceve ancora un puntatore **null** in un parametro di output.

Gli sviluppatori client devono evitare la possibilità che alcuni server restituiscano codici di errore diversi dai valori documentati. Per essere sicuri, è necessario assicurarsi che tutti i parametri di output contengano informazioni valide e soddisfino i criteri seguenti:

-   Tutti i puntatori sono non **null**.
-   Il membro **VT** di qualsiasi struttura [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) non è uguale a VT \_ vuoto.

 

 