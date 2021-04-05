---
description: La tabella MsiDigitalCertificate archivia i certificati in formato di flusso binario e associa ogni certificato a una chiave primaria.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Tabella MsiDigitalCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4765dee433cfab989e79c7ef4663d8939381ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755415"
---
# <a name="msidigitalcertificate-table"></a>Tabella MsiDigitalCertificate

La tabella MsiDigitalCertificate archivia i certificati in formato di flusso binario e associa ogni certificato a una chiave primaria. La chiave primaria viene utilizzata per condividere i certificati tra più oggetti con firma digitale. Un certificato digitale è una credenziale che fornisce un mezzo per verificare l'identità. Per ulteriori informazioni, vedere la sezione relativa alla [crittografia](../seccrypto/cryptography-portal.md) del Software Development Kit (SDK [) di Microsoft](../seccrypto/digital-certificates.md) Windows.

Le tabelle [MsiDigitalSignature](msidigitalsignature-table.md) e MsiDigitalCertificate sono disponibili a partire dalla versione di Windows Installer 2,0.

Windows Installer possibile utilizzare le firme digitali come mezzo per rilevare le risorse danneggiate. Windows Installer versione 2,0 è in grado di verificare solo le firme digitali dei cabinet esterni e solo l'utilizzo delle tabelle [MsiDigitalSignature](msidigitalsignature-table.md) e MsiDigitalCertificate.

A partire da Windows Installer versione 3,0, l'Windows Installer può verificare le firme digitali delle patch (file con estensione msp) usando le tabelle [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate. Per ulteriori informazioni, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e l'applicazione di [patch a controllo dell'account utente (UAC)](user-account-control--uac--patching.md).

La tabella MsiDigitalCertificate include le colonne seguenti.



| Colonna             | Tipo                         | Chiave | Nullable |
|--------------------|------------------------------|-----|----------|
| DigitalCertificate | [Identificatore](identifier.md) | S   | N        |
| CertData           | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Identifica il certificato di firma digitale. Chiave primaria della tabella.

</dd> <dt>

<span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData
</dt> <dd>

Rappresentazione binaria del certificato digitale. La colonna CertData contiene la matrice di byte codificata di un contesto del certificato. Si tratta del membro **pbCertEncoded** della struttura [**del \_ contesto del certificato**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) . Il contesto del certificato può essere ottenuto chiamando [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)o importando un file con estensione cer.

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

[Tabella MsiDigitalSignature](msidigitalsignature-table.md)
</dt> <dt>

[Firme digitali e Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
