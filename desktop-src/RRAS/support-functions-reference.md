---
title: Informazioni di riferimento sulle funzioni di supporto
description: Le funzioni seguenti vengono fornite ai protocolli di routing da Gestione router.
ms.assetid: 4e88c9fe-f6ec-4f9c-88b1-8726e10d0f6d
keywords:
- Protocollo routing interfaccia RRAS, funzioni di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbaba49c5f7e4130491a50176d560ee565b0046
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473814"
---
# <a name="support-functions-reference"></a>Informazioni di riferimento sulle funzioni di supporto

Le funzioni seguenti vengono fornite ai protocolli di routing da Gestione router. Quando Gestione router chiama la funzione [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) (implementata dal protocollo di routing), gestione router passa il protocollo di routing a una struttura di [**\_ funzioni di supporto**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) che contiene i puntatori alle funzioni seguenti:

[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))

[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))

[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))

[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))

[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))

[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))

[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))

[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))

[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))

 

 