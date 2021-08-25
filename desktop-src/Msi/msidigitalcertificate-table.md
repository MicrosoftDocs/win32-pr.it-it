---
description: La tabella MsiDigitalCertificate archivia i certificati in formato di flusso binario e associa ogni certificato a una chiave primaria.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Tabella MsiDigitalCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443e5f27d13ebd823fa8e5362de474082d39e4b09b9e240b9ee16e9924342e41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828781"
---
# <a name="msidigitalcertificate-table"></a>Tabella MsiDigitalCertificate

La tabella MsiDigitalCertificate archivia i certificati in formato di flusso binario e associa ogni certificato a una chiave primaria. La chiave primaria viene usata per condividere i certificati tra più oggetti con firma digitale. Un certificato digitale è una credenziale che consente di verificare l'identità. Per altre informazioni, vedere [Certificati](../seccrypto/digital-certificates.md) digitali nella [sezione Crittografia](../seccrypto/cryptography-portal.md) di Microsoft Windows Software Development Kit (SDK).

Le [tabelle MsiDigitalSignature](msidigitalsignature-table.md) e MsiDigitalCertificate sono disponibili a partire da Windows Installer versione 2.0.

Windows Il programma di installazione può usare le firme digitali come mezzo per rilevare le risorse danneggiate. Windows La versione 2.0 del programma di installazione può verificare solo le firme digitali degli archivi esterni e solo tramite l'uso delle tabelle [MsiDigitalSignature](msidigitalsignature-table.md) e MsiDigitalCertificate.

A partire da Windows Installer versione 3.0, il programma di installazione di Windows può verificare le firme digitali delle patch (file con estensione msp) usando le tabelle [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate. Per altre informazioni, vedere [Linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e Applicazione di patch al controllo dell'account [utente.](user-account-control--uac--patching.md)

La tabella MsiDigitalCertificate contiene le colonne seguenti.



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

Rappresentazione binaria del certificato digitale. La colonna CertData contiene la matrice di byte codificata di un contesto di certificato. Si tratta del **membro pbCertEncoded** della [**struttura CERT \_ CONTEXT.**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) Il contesto del certificato può essere ottenuto chiamando [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)o importando un file cer.

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

[Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
