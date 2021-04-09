---
description: A partire da Windows 10, CNG fornisce il supporto per le curve ellittiche denominate seguenti (ANSI X 9.62, X 9.63, FIPS 186-2).
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: 'CNG: curve ellittiche denominate (Bcrypt.h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35092d463e6f83917d231a87659e690ffeb59fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878617"
---
# <a name="cng-named-elliptic-curves"></a>Curve ellittiche denominate CNG

A partire da Windows 10, CNG fornisce il supporto per le curve ellittiche denominate seguenti (ANSI X 9.62, X 9.63, FIPS 186-2).

<dl> <dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ecc \_ curva \_ 25519**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------|
| Nome              | curve25519                                                  |
| Standard          | [Curva 25519](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| Dimensione chiave (bit)   | 255                                                         |
| In grado di supportare TLS       |                                                             |
| Identificatori di oggetto | nessuno                                                        |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**\_ \_ BRAINPOOLP160R1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP160r1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 160                                                                                                               |
| In grado di supportare TLS       | No                                                                                                                |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.1                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP160T1 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP160t1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 160                                                                                                               |
| In grado di supportare TLS       | No                                                                                                                |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.2                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**\_ \_ BRAINPOOLP192R1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP192r1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 192                                                                                                               |
| In grado di supportare TLS       | No                                                                                                                |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.3                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**\_ \_ BRAINPOOLP192T1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP192t1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 192                                                                                                               |
| In grado di supportare TLS       | No                                                                                                                |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.4                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**\_ \_ BRAINPOOLP224R1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP224r1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 224                                                                                                               |
| In grado di supportare TLS       | No                                                                                                                |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.5                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**\_ \_ BRAINPOOLP224T1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP224t1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 224                                                                                                               |
| In grado di supportare TLS       | No                                                                                                                |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.6                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**\_ \_ BRAINPOOLP256R1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP256r1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 256                                                                                                               |
| In grado di supportare TLS       | Sì                                                                                                               |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.7                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**\_ \_ BRAINPOOLP256T1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP256t1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 256                                                                                                               |
| In grado di supportare TLS       | No                                                                                                                |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.8                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**\_ \_ BRAINPOOLP320R1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP320r1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 320                                                                                                               |
| In grado di supportare TLS       | No                                                                                                                |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.9                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ecc \_ curva \_ BRAINPOOLP32 0T1**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP320t1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 320                                                                                                               |
| In grado di supportare TLS       | No                                                                                                                |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.10                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP384R1 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP384r1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 384                                                                                                               |
| In grado di supportare TLS       | Sì                                                                                                               |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.11                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**\_ \_ BRAINPOOLP384T1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP384t1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 384                                                                                                               |
| In grado di supportare TLS       | No                                                                                                                |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.12                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**\_ \_ BRAINPOOLP512R1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP512r1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 512                                                                                                               |
| In grado di supportare TLS       | Sì                                                                                                               |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.13                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**\_ \_ BRAINPOOLP512T1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP512t1                                                                                                   |
| Standard          | [ECC. Brainpool curve e generazione di curva standard](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Dimensione chiave (bit)   | 512                                                                                                               |
| In grado di supportare TLS       | No                                                                                                                |
| Identificatori di oggetto | 1.3.36.3.3.2.8.1.1.14                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ \_ \_ EC192WAPI curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|----------------------------------------------------------------|
| Nome              | ec192wapi                                                      |
| Standard          | Standard nazionale cinese per LAN wireless (GB 15629.11-2003) |
| Dimensione chiave (bit)   | 192                                                            |
| In grado di supportare TLS       | No                                                             |
| Identificatori di oggetto | 1.2.156.11235.1.1.2.1                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**\_ \_ NISTP192 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nome              | nistP192                                                                                                                     |
| Standard          | [Curve ellittiche consigliate per l'uso del governo federale](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Dimensione chiave (bit)   | 192                                                                                                                          |
| In grado di supportare TLS       | Sì                                                                                                                          |
| Identificatori di oggetto | 1.2.840.10045.3.1.1                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ \_ \_ NISTP224 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nome              | nistP224                                                                                                                     |
| Standard          | [Curve ellittiche consigliate per l'uso del governo federale](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Dimensione chiave (bit)   | 224                                                                                                                          |
| In grado di supportare TLS       | Sì                                                                                                                          |
| Identificatori di oggetto | 1.3.132.0.33                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**\_ \_ NISTP256 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nome              | nistP256                                                                                                                     |
| Standard          | [Curve ellittiche consigliate per l'uso del governo federale](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Dimensione chiave (bit)   | 256                                                                                                                          |
| In grado di supportare TLS       | Sì                                                                                                                          |
| Identificatori di oggetto | 1.2.840.10045.3.1.7                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ \_ \_ NISTP384 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nome              | nistP384                                                                                                                     |
| Standard          | [Curve ellittiche consigliate per l'uso del governo federale](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Dimensione chiave (bit)   | 384                                                                                                                          |
| In grado di supportare TLS       | Sì                                                                                                                          |
| Identificatori di oggetto | 1.3.132.0.34                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**\_ \_ NISTP521 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nome              | nistP521                                                                                                                     |
| Standard          | [Curve ellittiche consigliate per l'uso del governo federale](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Dimensione chiave (bit)   | 521                                                                                                                          |
| In grado di supportare TLS       | Sì                                                                                                                          |
| Identificatori di oggetto | 1.3.132.0.35                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ \_ \_ NUMSP256T1 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nome              | numsP256t1                                                                                                                              |
| Standard          | [Specifica della selezione della curva e dei parametri della curva supportati in MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Dimensione chiave (bit)   | 256                                                                                                                                     |
| In grado di supportare TLS       | No                                                                                                                                      |
| Identificatori di oggetto | nessuno                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ \_ \_ NUMSP384T1 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nome              | numsP384t1                                                                                                                              |
| Standard          | [Specifica della selezione della curva e dei parametri della curva supportati in MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Dimensione chiave (bit)   | 384                                                                                                                                     |
| In grado di supportare TLS       | No                                                                                                                                      |
| Identificatori di oggetto | nessuno                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**\_ \_ NUMSP512T1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nome              | numsP512t1                                                                                                                              |
| Standard          | [Specifica della selezione della curva e dei parametri della curva supportati in MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Dimensione chiave (bit)   | 512                                                                                                                                     |
| In grado di supportare TLS       | No                                                                                                                                      |
| Identificatori di oggetto | nessuno                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ \_ \_ SECP160K1 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP160k1                                                                       |
| Standard          | [Parametri di dominio curva ellittica consigliati](https://www.secg.org/sec2-v2.pdf) |
| Dimensione chiave (bit)   | 160                                                                             |
| In grado di supportare TLS       | Sì                                                                             |
| Identificatori di oggetto | 1.3.132.0.9                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP160r1                                                                       |
| Standard          | [Parametri di dominio curva ellittica consigliati](https://www.secg.org/sec2-v2.pdf) |
| Dimensione chiave (bit)   | 160                                                                             |
| In grado di supportare TLS       | Sì                                                                             |
| Identificatori di oggetto | 1.3.132.0.8                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP160r2                                                                       |
| Standard          | [Parametri di dominio curva ellittica consigliati](https://www.secg.org/sec2-v2.pdf) |
| Dimensione chiave (bit)   | 160                                                                             |
| In grado di supportare TLS       | Sì                                                                             |
| Identificatori di oggetto | 1.3.132.0.30                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**\_ \_ SECP192K1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP192k1                                                                       |
| Standard          | [Parametri di dominio curva ellittica consigliati](https://www.secg.org/sec2-v2.pdf) |
| Dimensione chiave (bit)   | 192                                                                             |
| In grado di supportare TLS       | Sì                                                                             |
| Identificatori di oggetto | 1.3.132.0.31                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ \_ \_ SECP192R1 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP192r1                                                                       |
| Standard          | [Parametri di dominio curva ellittica consigliati](https://www.secg.org/sec2-v2.pdf) |
| Dimensione chiave (bit)   | 192                                                                             |
| In grado di supportare TLS       | Sì                                                                             |
| Identificatori di oggetto | 1.2.840.10045.3.1.1                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**\_ \_ SECP224K1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP224k1                                                                       |
| Standard          | [Parametri di dominio curva ellittica consigliati](https://www.secg.org/sec2-v2.pdf) |
| Dimensione chiave (bit)   | 224                                                                             |
| In grado di supportare TLS       | Sì                                                                             |
| Identificatori di oggetto | 1.3.132.0.32                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**\_ \_ SECP224R1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP224r1                                                                       |
| Standard          | [Parametri di dominio curva ellittica consigliati](https://www.secg.org/sec2-v2.pdf) |
| Dimensione chiave (bit)   | 224                                                                             |
| In grado di supportare TLS       | Sì                                                                             |
| Identificatori di oggetto | 1.3.132.0.33                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**\_ \_ SECP256K1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP256k1                                                                       |
| Standard          | [Parametri di dominio curva ellittica consigliati](https://www.secg.org/sec2-v2.pdf) |
| Dimensione chiave (bit)   | 256                                                                             |
| In grado di supportare TLS       | Sì                                                                             |
| Identificatori di oggetto | 1.3.132.0.10                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**\_ \_ SECP256R1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP256r1                                                                       |
| Standard          | [Parametri di dominio curva ellittica consigliati](https://www.secg.org/sec2-v2.pdf) |
| Dimensione chiave (bit)   | 256                                                                             |
| In grado di supportare TLS       | Sì                                                                             |
| Identificatori di oggetto | 1.2.840.10045.3.1.7                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ \_ \_ SECP384R1 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP384r1                                                                       |
| Standard          | [Parametri di dominio curva ellittica consigliati](https://www.secg.org/sec2-v2.pdf) |
| Dimensione chiave (bit)   | 384                                                                             |
| In grado di supportare TLS       | Sì                                                                             |
| Identificatori di oggetto | 1.3.132.0.34                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**\_ \_ SECP521R1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP521r1                                                                       |
| Standard          | [Parametri di dominio curva ellittica consigliati](https://www.secg.org/sec2-v2.pdf) |
| Dimensione chiave (bit)   | 521                                                                             |
| In grado di supportare TLS       | Sì                                                                             |
| Identificatori di oggetto | 1.3.132.0.35                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**\_ \_ WTLS12 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|--------------|
| Nome              | wtls12       |
| Standard          | WTLS         |
| Dimensione chiave (bit)   | 224          |
| In grado di supportare TLS       | No           |
| Identificatori di oggetto | 1.3.132.0.33 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**\_ \_ WTLS7 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|--------------|
| Nome              | wtls7        |
| Standard          | WTLS         |
| Dimensione chiave (bit)   | 160          |
| In grado di supportare TLS       | No           |
| Identificatori di oggetto | 1.3.132.0.30 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ \_ \_ WTLS9 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------|
| Nome              | wtls9         |
| Standard          | WTLS          |
| Dimensione chiave (bit)   | 160           |
| In grado di supportare TLS       | No            |
| Identificatori di oggetto | 2.23.43.1.4.9 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**\_ \_ X962P192V1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------|
| Nome              | x962P192v1          |
| Standard          | 9.62 ANSI X          |
| Dimensione chiave (bit)   | 192                 |
| In grado di supportare TLS       | No                  |
| Identificatori di oggetto | 1.2.840.10045.3.1.1 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ \_ \_ X962P192V2 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------|
| Nome              | x962P192v2          |
| Standard          | 9.62 ANSI X          |
| Dimensione chiave (bit)   | 192                 |
| In grado di supportare TLS       | No                  |
| Identificatori di oggetto | 1.2.840.10045.3.1.2 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**\_ \_ X962P192V3 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------|
| Nome              | x962P192v3          |
| Standard          | 9.62 ANSI X          |
| Dimensione chiave (bit)   | 192                 |
| In grado di supportare TLS       | No                  |
| Identificatori di oggetto | 1.2.840.10045.3.1.3 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ \_ \_ X962P239V1 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------|
| Nome              | x962P239v1          |
| Standard          | 9.62 ANSI X          |
| Dimensione chiave (bit)   | 239                 |
| In grado di supportare TLS       | No                  |
| Identificatori di oggetto | 1.2.840.10045.3.1.4 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ \_ \_ X962P239V2 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------|
| Nome              | x962P239v2          |
| Standard          | 9.62 ANSI X          |
| Dimensione chiave (bit)   | 239                 |
| In grado di supportare TLS       | No                  |
| Identificatori di oggetto | 1.2.840.10045.3.1.5 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ \_ \_ X962P239V3 curva ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------|
| Nome              | x962P239v3          |
| Standard          | 9.62 ANSI X          |
| Dimensione chiave (bit)   | 239                 |
| In grado di supportare TLS       | No                  |
| Identificatori di oggetto | 1.2.840.10045.3.1.6 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**\_ \_ X962P256V1 curva BCRYPT \_ ecc**</dt> <dd> <dl> <dt> 

| Requisito | Valore |
|-------------------|---------------------|
| Nome              | x962P256v1          |
| Standard          | 9.62 ANSI X          |
| Dimensione chiave (bit)   | 256                 |
| In grado di supportare TLS       | No                  |
| Identificatori di oggetto | 1.2.840.10045.3.1.7 |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Per usare una curva denominata, chiamare [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) usando l'algoritmo **BCRYPT \_ ECDSA \_** o l'algoritmo **BCRYPT \_ ECDH \_** come ID algoritmo. Chiamare quindi [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) e impostare la proprietà **BCRYPT \_ ecc \_ curve \_ Name** su una delle curve indicate sopra o tutte le curve denominate registrate nel computer, come illustrato dal `certutil -displayEccCurve` comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




