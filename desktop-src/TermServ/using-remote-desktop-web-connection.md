---
title: Uso del controllo ActiveX Desktop remoto
description: Come è possibile utilizzare il controllo ActiveX Desktop remoto per personalizzare l'esperienza utente Servizi Desktop remoto.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto utilizzando il controllo ActiveX Desktop remoto
- Connessione Web Desktop remoto Servizi Desktop remoto utilizzando
- Remote Desktop Protocol Servizi Desktop remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297923"
---
# <a name="using-the-remote-desktop-activex-control"></a>Uso del controllo ActiveX Desktop remoto

Negli argomenti seguenti sono contenute informazioni su come utilizzare il controllo ActiveX Desktop remoto per personalizzare l'esperienza utente Servizi Desktop remoto.

Il controllo ActiveX Desktop remoto è disponibile nei formati seguenti:

-   **Il controllo eseguibile tramite script**, implementa interfacce sicure per lo scripting. Questo formato del controllo può essere utilizzato da client Web o script (ad esempio VBScript).
-   **Il controllo** non utilizzabile per gli script: offre funzionalità aggiuntive che non sono sicure per lo scripting. Questo formato del controllo può essere utilizzato da codice nativo o gestito, ma non può essere utilizzato dai client Web o dagli host solo script.

Nell'elenco seguente sono inclusi i **CLSID** per i diversi controlli per diverse versioni del sistema operativo. Ogni **CLSID** è compatibile con versioni di sistema successive. Il **CLSID** per il controllo di scripting in Windows Vista, ad esempio, funzionerà con versioni di sistema successive, ad esempio Windows 7.



| Versione sistema                          | CLSID controllo con script             | CLSID di controllo non conscriptbile          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| Windows 8.1, Windows Server 2012 R2     | 301B94BA-5D25-4A12-BFFE-3B6E7A616585 | 8B918B82-7985-4C24-89DF-C33AD2BBFBCD |
| Windows 8, Windows Server 2012          | 5F681803-2900-4C43-A1CC-CF405404A676 | A3BC03A0-041D-42E3-AD22-882B7865C9C5 |
| Windows 7, Windows Server 2008          | A9D7038D-B5ED-472E-9C47-94BEA90A5910 | 54D38BF7-B1EF-4479-9674-1BD6EA465258 |
| Windows Vista con Service Pack 1 (SP1) | 7390F3D8-0439-4C05-91E3-CF5CB290C3D0 | D2EA46A7-C2BF-426B-AF24-E19C44456399 |
| Windows Vista                           | 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2 | 4EB2F086-C818-447E-B32C-C51CE2B30D31 |



 

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Incorporamento del controllo ActiveX Desktop remoto in una pagina Web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

Esempio che illustra l'uso delle interfacce di scripting.

</dd> <dt>

[Implementazione di canali virtuali tramite script tramite Connessione Web Desktop remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

Esempi di codice che illustrano i passaggi per l'implementazione di canali virtuali utilizzabili tramite script con Connessione Web Desktop remoto.

</dd> <dt>

[Uso del controllo ActiveX Desktop remoto con i canali virtuali](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

Se è stata abilitata un'applicazione per i canali virtuali nella distribuzione di Servizi Desktop remoto, è possibile rendere disponibile questa applicazione per i computer client.

</dd> <dt>

[Pagina Web di esempio inclusa con il controllo ActiveX Desktop remoto](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

Una pagina Web di esempio (Default.htm) si trova nella directory in cui è installato Connessione Web Desktop remoto.

</dd> <dt>

[Fornire la sicurezza del client RDP](providing-for-rdp-client-security.md)
</dt> <dd>

Alcune proprietà dell'oggetto Desktop remoto controllo ActiveX sono limitate a specifiche aree di sicurezza URL di Internet Explorer.

</dd> <dt>

[Disabilitazione delle funzionalità di Servizi Desktop remoto](disabling-terminal-services-features.md)
</dt> <dd>

Per una maggiore sicurezza, è possibile scegliere di disabilitare Servizi Desktop remoto funzionalità.

</dd> </dl>

Per ulteriori informazioni sulla pagina Web di esempio inclusa nell'installazione del controllo ActiveX Desktop remoto, vedere [la pagina Web di esempio inclusa nel controllo activex desktop remoto](sample-web-page-included-with-the-remote-desktop-activex-control.md).

 

 




