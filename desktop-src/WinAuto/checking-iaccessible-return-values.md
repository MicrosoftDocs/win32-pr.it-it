---
title: Controllo dei valori restituiti IAccessible
description: Gli sviluppatori client non devono basarsi sulle macro Component Object Model (COM) SUCCEEDED e FAILED per testare i valori restituiti IAccessible, perché i valori diversi da S OK sono considerati un \_ esito positivo.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1df43a316898ceeb751b114251ca8fbc91a8fc5360558a3929bcc3ecc47cce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759631"
---
# <a name="checking-iaccessible-return-values"></a>Controllo dei valori restituiti IAccessible

Gli sviluppatori client non devono basarsi sulle macro Component Object Model (COM) [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) e [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) per testare i valori restituiti [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) perché i valori diversi da S OK sono considerati un \_ esito positivo. Ad esempio, un metodo può restituire S FALSE, che viene considerato un esito positivo dalla macro SUCCEEDED, ma riceve comunque un \_ **puntatore NULL** in un  parametro di output.

Gli sviluppatori client devono proteggersi dalla possibilità che alcuni server restituiranno codici di errore diversi dai valori documentati. Per essere sicuri, è necessario assicurarsi che tutti i parametri di output contengano informazioni valide e soddisfino i criteri seguenti:

-   Tutti i puntatori sono non **NULL.**
-   Il **membro vt** di qualsiasi [struttura VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) non è uguale a VT \_ EMPTY.

 

 