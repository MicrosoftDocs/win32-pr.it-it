---
description: Il modello di sicurezza usato nel protocollo Microsoft SMB è identico a quello usato da altre varianti di SMB ed è costituito da due livelli di sicurezza&\# 8212;utente e condivisione.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Autenticazione del protocollo SMB Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b924b225a129a88d71d7906d815d330c74195252e40c9bc798efdb7df1948f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914681"
---
# <a name="microsoft-smb-protocol-authentication"></a>Autenticazione del protocollo SMB Microsoft

Il modello di sicurezza usato nel protocollo Microsoft SMB è identico a quello usato da altre varianti di SMB ed è costituito da due livelli di sicurezza: utente e condivisione. Una condivisione è un file, una directory o una stampante accessibile dai client del protocollo Microsoft SMB.

L'autenticazione a livello di utente indica che il client che tenta di accedere a una condivisione in un server deve fornire un nome utente e una password. Dopo l'autenticazione, l'utente può quindi accedere a tutte le condivisioni in un server non protetto anche dalla sicurezza a livello di condivisione. Questo livello di sicurezza consente agli amministratori di sistema di determinare in modo specifico quali utenti e gruppi possono accedere a una condivisione.

L'autenticazione a livello di condivisione indica che l'accesso a una condivisione è controllato da una password assegnata solo a tale condivisione. A differenza della sicurezza a livello di utente, questo livello di sicurezza non richiede un nome utente per l'autenticazione e non viene stabilita alcuna identità utente.

In entrambi questi livelli di sicurezza, la password viene crittografata prima di essere inviata al server. [NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) e la crittografia precedente di LAN Manager (LM) sono supportati dal protocollo Microsoft SMB. Entrambi i metodi di crittografia usano l'autenticazione challenge-response, in cui il server invia al client una stringa casuale e il client restituisce una stringa di risposta calcolata che dimostra che il client ha credenziali sufficienti per l'accesso.

 

 
