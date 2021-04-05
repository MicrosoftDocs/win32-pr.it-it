---
title: Linee guida sui client
description: Gli sviluppatori client devono utilizzare le funzionalità seguenti per ottenere informazioni sugli elementi dell'interfaccia utente
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "103956137"
---
# <a name="client-guidelines"></a>Linee guida sui client

Gli sviluppatori client devono utilizzare le funzionalità seguenti per ottenere informazioni sugli elementi dell'interfaccia utente:

-   Per ottenere un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per gli oggetti, chiamare [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).
-   Per esaminare e modificare gli oggetti accessibili, utilizzare le proprietà e i metodi di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
-   Per ricevere [winEvents](winevents-overview.md), chiamare [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) per registrare una funzione di callback WinEvent per gli eventi rilevanti per l'applicazione client.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Come i client ottengono gli ID figlio](how-clients-obtain-child-ids.md)

 

 




