---
title: Classe MDM_VPNv2_CryptographySuite03
description: La \_ classe MDM VPNv2 \_ CryptographySuite03 contiene informazioni di crittografia per il profilo VPN nativo.
ms.assetid: d8d16d43-bd54-4ca8-a850-ce48390df7d6
keywords:
- Classe MDM_VPNv2_CryptographySuite03
- Classe MDM_VPNv2_CryptographySuite03, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_CryptographySuite03
- MDM_VPNv2_CryptographySuite03.InstanceID
- MDM_VPNv2_CryptographySuite03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553f2dcddd4d7c7e0926945a80f74f6aba2a9467
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476769"
---
# <a name="mdm_vpnv2_cryptographysuite03-class"></a>\_Classe MDM VPNv2 \_ CryptographySuite03

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe **MDM \_ VPNv2 \_ CryptographySuite03** contiene informazioni di crittografia per il profilo VPN nativo.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_CryptographySuite03
{
  string InstanceID;
  string ParentID;
  string AuthenticationTransformConstants;
  string CipherTransformConstants;
  string EncryptionMethod;
  string IntegrityCheckMethod;
  string DHGroup;
  string PfsGroup;
};
```

## <a name="members"></a>Members

La classe **MDM \_ VPNv2 \_ CryptographySuite03** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **MDM \_ VPNv2 \_ CryptographySuite03** dispone di queste proprietà.

<dl> <dt>

[AuthenticationTransformConstants](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-authenticationtransformconstants)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[CipherTransformConstants](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-ciphertransformconstants)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[DHGroup](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-dhgroup)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[EncryptionMethod](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-encryptionmethod)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nodo contenente le proprietà dei tunnel IPSec.

</dd> <dt>

[IntegrityCheckMethod](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-integritycheckmethod)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"

</dd> <dt>

[PfsGroup](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-pfsgroup)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

