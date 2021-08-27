---
title: Codici di errore LDAP per ADSI
description: Quando un server LDAP genera un errore e lo passa al client, l'errore viene convertito in una stringa dal client LDAP.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6280784d8bf9fc9c692cb38f1ca2d0e76646b1d2a3d464e516f03e7ac682fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005511"
---
# <a name="ldap-error-codes-for-adsi"></a>Codici di errore LDAP per ADSI

Quando un server LDAP genera un errore e lo passa al client, l'errore viene convertito in una stringa dal client LDAP.

Questo metodo è simile ai [codici di errore Win32 per ADSI.](win32-error-codes-for-adsi.md) In questo esempio il codice di errore client è l'errore WIN32 0x80072020.

**Per determinare i codici di errore LDAP per ADSI**

1.  Eliminare 8007 dal codice di errore WIN32. Nell'esempio il valore esadecimale rimanente è 2020.
2.  Convertire il valore esadecimale rimanente in un valore decimale. Nell'esempio il valore esadecimale rimanente 2020 viene convertito nel valore decimale 8224.
3.  Cercare nel file WinError.h la definizione del valore decimale. Nell'esempio, 8224L corrisponde all'errore **ERROR \_ DS \_ OPERATIONS \_ ERROR**.
4.  Sostituire il prefisso **ERROR \_ DS** con **\_ LDAP**. Nell'esempio la nuova definizione è **LDAP \_ OPERATIONS \_ ERROR**.
5.  Cercare nel file Winldap.h il valore della definizione di errore LDAP. Nell'esempio il valore di **LDAP \_ OPERATIONS \_ ERROR** nel file Winldap.h è 0x01.

 

 




