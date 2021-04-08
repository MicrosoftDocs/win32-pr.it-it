---
title: Attributi multipoint in WSAPROTOCOL_INFO
description: Gli attributi multipoint nella struttura delle informazioni di WSAPROTOCOL \_ includono il \_ supporto di XP1 \_ MultiPoint, il \_ \_ piano di controllo multipoint XP1 e il \_ \_ \_ piano dati multipoint XP1 \_ .
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baedcd07f53db462eb090217b53d93a1a4aa8c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751439"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a>Attributi multipoint in WSAPROTOCOL_INFO

Tre parametri di attributo sono definiti nella struttura delle [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per distinguere i diversi schemi utilizzati rispettivamente nel controllo e nei piani dati:

-   XP1 \_ supporta \_ multipoint con un valore 1 indica che questa voce di protocollo supporta le comunicazioni multipoint e che i due parametri seguenti sono significativi.
-   \_ \_ \_ Il piano di controllo multipoint XP1 indica se il piano di controllo è radice (valore = 1) o non radice (valore = 0).
-   \_ \_ Il piano dati multipoint XP1 \_ indica se il piano dati è radice (valore = 1) o non radice (valore = 0).

Sono presenti due voci di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) se un protocollo multipoint supporta i piani dati radice e non radice, una voce per ogni.

 

 
