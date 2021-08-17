---
title: Attributi multipunto in WSAPROTOCOL_INFO
description: Gli attributi multipoint nella struttura WSAPROTOCOL INFO includono \_ XP1 \_ SUPPORT \_ MULTIPOINT, XP1 \_ MULTIPOINT \_ CONTROL PLANE e \_ XP1 \_ MULTIPOINT DATA \_ \_ PLANE.
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1275b6da00258be10b071bc9b2399abaf5dd608583f3d81a0fdb16af493824ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741105"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a>Attributi multipunto in WSAPROTOCOL_INFO

Nella struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) vengono definiti tre parametri di attributo per distinguere rispettivamente i diversi schemi usati nei piani di controllo e di dati:

-   XP1 SUPPORT MULTIPOINT con valore 1 indica che questa voce di protocollo supporta le comunicazioni multipoint e che i \_ due parametri seguenti sono \_ significativi.
-   XP1 MULTIPOINT CONTROL PLANE indica se il piano di controllo è \_ \_ \_ rooted (valore = 1) o non rooted (valore = 0).
-   XP1 MULTIPOINT DATA PLANE indica se il piano dati è \_ \_ \_ rooted (valore = 1) o non rooted (valore = 0).

Due [**voci WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) sarebbero presenti se un protocollo multipoint supportasse sia piani dati rooted che nonrooted, una voce per ognuna.

 

 
