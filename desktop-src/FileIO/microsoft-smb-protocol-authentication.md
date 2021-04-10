---
description: Il modello di sicurezza usato nel protocollo SMB Microsoft è identico a quello usato da altre varianti di SMB ed è costituito da due livelli di sicurezza&\# 8212; utente e condivisione.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Autenticazione del protocollo SMB Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879114"
---
# <a name="microsoft-smb-protocol-authentication"></a>Autenticazione del protocollo SMB Microsoft

Il modello di sicurezza usato nel protocollo SMB Microsoft è identico a quello usato da altre varianti di SMB ed è costituito da due livelli di sicurezza: utente e condivisione. Una condivisione è un file, una directory o una stampante a cui è possibile accedere dai client del protocollo SMB Microsoft.

L'autenticazione a livello di utente indica che il client che tenta di accedere a una condivisione in un server deve fornire un nome utente e una password. Una volta eseguita l'autenticazione, l'utente può accedere a tutte le condivisioni in un server non protette anche dalla sicurezza a livello di condivisione. Questo livello di sicurezza consente agli amministratori di sistema di determinare in modo specifico quali utenti e gruppi possono accedere a una condivisione.

L'autenticazione a livello di condivisione indica che l'accesso a una condivisione è controllato da una password assegnata solo a tale condivisione. Diversamente dalla sicurezza a livello di utente, questo livello di sicurezza non richiede un nome utente per l'autenticazione e non viene stabilita alcuna identità utente.

In entrambi i livelli di sicurezza, la password viene crittografata prima che venga inviata al server. [NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) e la crittografia precedente di LAN Manager (lm) sono supportati dal protocollo Microsoft SMB. Entrambi i metodi di crittografia utilizzano l'autenticazione di richiesta-risposta, in cui il server invia al client una stringa casuale e il client restituisce una stringa di risposta calcolata che dimostra che il client dispone di credenziali sufficienti per l'accesso.

 

 
