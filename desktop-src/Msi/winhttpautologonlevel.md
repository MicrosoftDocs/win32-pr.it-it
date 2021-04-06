---
description: Il criterio di accesso automatico (accesso automatico) determina quando è accettabile che WinHTTP includa le credenziali predefinite in una richiesta al server.
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: WinHttpAutoLogonLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7760faa94e24b7fe5b33717c504b03e4de42c0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882697"
---
# <a name="winhttpautologonlevel"></a>WinHttpAutoLogonLevel

Il criterio di accesso automatico (accesso automatico) determina quando è accettabile che *WinHTTP* includa le credenziali predefinite in una richiesta al server.

È possibile impostare questo valore su **L** per il livello di sicurezza automatico WinHTTP ( **\_ \_ \_ \_ bassa**), impostare su **M** per il livello di sicurezza di WinHTTP AutoLogon **\_ \_ \_ \_ media** e impostare su **H** per il **livello di sicurezza con \_ logo automatico WinHTTP \_ \_ \_ alto**. Il livello predefinito è **la \_ \_ \_ \_ media del livello di sicurezza WinHTTP AutoLogon**. Per ulteriori informazioni sui criteri di accesso automatici, vedere la sezione relativa all' [autenticazione in WinHTTP](../winhttp/authentication-in-winhttp.md).

**Windows 8 e Windows Server 2012:** Questo criterio richiede l'esecuzione di Windows Installer in Windows 8 o Windows Server 2012 e non è disponibile in tutte le versioni precedenti di Windows.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ SZ**

 

 
