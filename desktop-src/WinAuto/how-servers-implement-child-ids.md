---
title: Modalità di implementazione degli ID figlio da server
description: Gli sviluppatori di server possono assegnare gli ID figlio sia agli elementi semplici che agli oggetti accessibili. Tuttavia, l'approccio consigliato consiste nel supportare l'interfaccia COM (standard Component Object Model) IEnumVARIANT in tutti gli oggetti accessibili che dispongono di elementi figlio.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963255"
---
# <a name="how-servers-implement-child-ids"></a>Modalità di implementazione degli ID figlio da server

Gli sviluppatori di server possono assegnare gli ID figlio sia agli elementi semplici che agli oggetti accessibili. Tuttavia, l'approccio consigliato consiste nel supportare l'interfaccia COM (standard Component Object Model) [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) in tutti gli oggetti accessibili che dispongono di elementi figlio.

Se si implementa [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), è necessario:

-   Enumerare tutti gli elementi figlio, sia semplici che oggetti accessibili. Fornire gli ID figlio per tutti gli elementi semplici e fornire [**IDispatch**](idispatch-interface.md) a ogni oggetto accessibile.
-   Per gli oggetti accessibili, impostare il membro **VT** della [**variante**](variant-structure.md) sul \_ Dispatch VT. Il membro **pdispVal** deve contenere un puntatore all'interfaccia [**IDispatch**](idispatch-interface.md) . Si noti che il **Variant** viene allocato e liberato dal client.
-   Per gli elementi semplici, l'ID figlio è qualsiasi numero intero positivo a 32 bit. Si noti che gli Integer zero e negativi sono riservati da Microsoft Active Accessibility. Impostare il membro **VT** della struttura [**Variant**](variant-structure.md) su VT \_ I4 e il membro **LVAL** sull'ID figlio.

Se non si supporta [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), è necessario assegnare gli ID figlio e numerare gli elementi figlio in ogni oggetto a partire da uno in sequenza.

È consigliabile che i client usino la funzione Microsoft Active Accessibility [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) invece di chiamare direttamente l'interfaccia [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) del server.

 

 