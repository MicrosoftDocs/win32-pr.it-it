---
description: La tabella MsiDigitalSignature contiene le informazioni sulla firma per ogni oggetto con firma digitale nel database di installazione.
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: Tabella MsiDigitalSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ec22b9a399b6248fd3b2781e1ac8d7ae14324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310523"
---
# <a name="msidigitalsignature-table"></a>Tabella MsiDigitalSignature

La tabella MsiDigitalSignature contiene le informazioni sulla firma per ogni oggetto con firma digitale nel database di installazione.

Le tabelle MsiDigitalSignature e [MsiDigitalCertificate](msidigitalcertificate-table.md) sono disponibili a partire dalla versione di Windows Installer 2,0.

Windows Installer versione può utilizzare le firme digitali come mezzo per rilevare le risorse danneggiate. Windows Installer 2,0 può verificare solo le firme digitali dei cabinet esterni e solo l'utilizzo delle tabelle MsiDigitalSignature e [MsiDigitalCertificate](msidigitalcertificate-table.md) .

A partire da Windows Installer 3,0, il Windows Installer può verificare le firme digitali delle patch (file con estensione msp) usando le tabelle [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate. Per ulteriori informazioni, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e l'applicazione di [patch a controllo dell'account utente (UAC)](user-account-control--uac--patching.md).

La tabella MsiDigitalSignature include le colonne seguenti.



| Colonna               | Tipo                         | Chiave | Nullable |
|----------------------|------------------------------|-----|----------|
| Tabella                | [Identificatore](identifier.md) | S   | N        |
| SignObject           | [Text](text.md)             | S   | N        |
| DigitalCertificate\_ | [Identificatore](identifier.md) | N   | N        |
| Hash                 | [Binario](binary.md)         | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Con la versione di Windows Installer 2,0, la voce in questo campo deve essere "media" per la [tabella dei supporti](media-table.md). Il programma di installazione verifica solo le firme digitali sulle voci multimediali del cabinet esterno. Questa colonna e la colonna SignObject specificano insieme la risorsa con firma digitale.

</dd> <dt>

<span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject
</dt> <dd>

Chiave esterna nella chiave primaria della tabella specificata dalla colonna della tabella. Questa colonna e la colonna della tabella specificano insieme la risorsa con firma digitale.

</dd> <dt>

<span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_
</dt> <dd>

Chiave esterna nella [tabella MsiDigitalCertificate](msidigitalcertificate-table.md). Identifica il certificato che deve esistere nel file affinché l'azione associata abbia esito positivo. È sempre necessario che la risorsa (o oggetto) corrisponda a questo certificato nella tabella MsiDigitalCertificate.

</dd> <dt>

<span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash
</dt> <dd>

In questo campo immettere l'hash di riferimento della risorsa (o oggetto) da verificare rispetto all'hash effettivo della risorsa (o oggetto) ottenuta in fase di esecuzione. Se è necessario verificare solo il certificato, il campo hash può essere null. Si noti che il formato dell'hash dipende dal tipo di risorsa (o oggetto) firmato.

La colonna hash contiene la rappresentazione binaria dell'hash. Il contenuto effettivo è il membro **pbData** della struttura [**\_ \_ blob hash Crypt**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) , che fa parte della struttura del **\_ BLOB CryptoAPI** . Questa operazione può essere ottenuta chiamando [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) o [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[Tabella MsiDigitalCertificate](msidigitalcertificate-table.md)
</dt> <dt>

[Firme digitali e Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
