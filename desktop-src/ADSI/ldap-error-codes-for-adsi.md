---
title: Codici di errore LDAP per ADSI
description: Quando un server LDAP genera un errore e passa l'errore al client, l'errore viene quindi convertito in una stringa dal client LDAP.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855285"
---
# <a name="ldap-error-codes-for-adsi"></a>Codici di errore LDAP per ADSI

Quando un server LDAP genera un errore e passa l'errore al client, l'errore viene quindi convertito in una stringa dal client LDAP.

Questo metodo è simile ai [codici di errore Win32 per ADSI](win32-error-codes-for-adsi.md). In questo esempio, il codice di errore del client è l'errore WIN32 0x80072020.

**Per determinare i codici di errore LDAP per ADSI**

1.  Eliminare 8007 dal codice di errore WIN32. Nell'esempio, il valore esadecimale rimanente è 2020.
2.  Converte il valore esadecimale rimanente in un valore decimale. Nell'esempio, il valore esadecimale rimanente 2020 viene convertito nel valore decimale 8224.
3.  Cercare nel file WinError. h la definizione del valore decimale. Nell'esempio, 8224L corrisponde all'errore di **\_ \_ operazioni \_ DS** Error Error.
4.  Sostituire l'errore di prefisso **\_ DS** con **LDAP \_**. Nell'esempio, la nuova definizione è un **\_ \_ errore di operazioni LDAP**.
5.  Cercare nel file Winldap. h il valore della definizione di errore LDAP. Nell'esempio, il valore dell' **errore di \_ operazioni \_ LDAP** nel file Winldap. h è 0x01.

 

 




