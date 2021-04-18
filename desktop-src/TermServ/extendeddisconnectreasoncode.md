---
title: Enumerazione ExtendedDisconnectReasonCode
description: Definisce le informazioni estese sul motivo del controllo per la disconnessione.
ms.assetid: E73E73B4-6C6B-4270-A1BD-947FA6D7B31B
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto enumerazione ExtendedDisconnectReasonCode
topic_type:
- apiref
api_name:
- ExtendedDisconnectReasonCode
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657d0faee03ca37b9a5a49b95b978a24b0c8955c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302480"
---
# <a name="extendeddisconnectreasoncode-enumeration"></a><span data-ttu-id="32e5f-104">Enumerazione ExtendedDisconnectReasonCode</span><span class="sxs-lookup"><span data-stu-id="32e5f-104">ExtendedDisconnectReasonCode enumeration</span></span>

<span data-ttu-id="32e5f-105">Definisce le informazioni estese sul motivo del controllo per la disconnessione.</span><span class="sxs-lookup"><span data-stu-id="32e5f-105">Defines extended information about the control's reason for disconnection.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e5f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32e5f-106">Syntax</span></span>


```C++
typedef enum _ExtendedDisconnectReasonCode { 
  exDiscReasonNoInfo                            = 0,
  exDiscReasonAPIInitiatedDisconnect            = 1,
  exDiscReasonAPIInitiatedLogoff                = 2,
  exDiscReasonServerIdleTimeout                 = 3,
  exDiscReasonServerLogonTimeout                = 4,
  exDiscReasonReplacedByOtherConnection         = 5,
  exDiscReasonOutOfMemory                       = 6,
  exDiscReasonServerDeniedConnection            = 7,
  exDiscReasonServerDeniedConnectionFips        = 8,
  exDiscReasonServerInsufficientPrivileges      = 9,
  exDiscReasonServerFreshCredsRequired          = 10,
  exDiscReasonRpcInitiatedDisconnectByUser      = 11,
  exDiscReasonLogoffByUser                      = 2,
  exDiscReasonLicenseInternal                   = 256,
  exDiscReasonLicenseNoLicenseServer            = 257,
  exDiscReasonLicenseNoLicense                  = 258,
  exDiscReasonLicenseErrClientMsg               = 259,
  exDiscReasonLicenseHwidDoesntMatchLicense     = 260,
  exDiscReasonLicenseErrClientLicense           = 261,
  exDiscReasonLicenseCantFinishProtocol         = 262,
  exDiscReasonLicenseClientEndedProtocol        = 263,
  exDiscReasonLicenseErrClientEncryption        = 264,
  exDiscReasonLicenseCantUpgradeLicense         = 265,
  exDiscReasonLicenseNoRemoteConnections        = 266,
  exDiscReasonLicenseCreatingLicStoreAccDenied  = 267,
  exDiscReasonRdpEncInvalidCredentials          = 768,
  exDiscReasonProtocolRangeStart                = 4096,
  exDiscReasonProtocolRangeEnd                  = 32767
} ExtendedDisconnectReasonCode;
```



## <a name="constants"></a><span data-ttu-id="32e5f-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="32e5f-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="32e5f-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span><span class="sxs-lookup"><span data-stu-id="32e5f-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-109">Non sono disponibili informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="32e5f-109">No additional information is available.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span><span class="sxs-lookup"><span data-stu-id="32e5f-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-111">La disconnessione è stata avviata da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="32e5f-111">An application initiated the disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span><span class="sxs-lookup"><span data-stu-id="32e5f-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-113">Un'applicazione ha disconnesso il client.</span><span class="sxs-lookup"><span data-stu-id="32e5f-113">An application logged off the client.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="32e5f-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-115">Il server ha disconnesso il client perché il client è rimasto inattivo per un periodo di tempo più lungo rispetto al periodo di timeout designato.</span><span class="sxs-lookup"><span data-stu-id="32e5f-115">The server has disconnected the client because the client has been idle for a period of time longer than the designated time-out period.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span><span class="sxs-lookup"><span data-stu-id="32e5f-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-117">Il server ha disconnesso il client perché il client ha superato il periodo designato per la connessione.</span><span class="sxs-lookup"><span data-stu-id="32e5f-117">The server has disconnected the client because the client has exceeded the period designated for connection.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span><span class="sxs-lookup"><span data-stu-id="32e5f-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-119">La connessione del client è stata sostituita da un'altra connessione.</span><span class="sxs-lookup"><span data-stu-id="32e5f-119">The client's connection was replaced by another connection.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span><span class="sxs-lookup"><span data-stu-id="32e5f-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-121">Memoria non disponibile.</span><span class="sxs-lookup"><span data-stu-id="32e5f-121">No memory is available.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span><span class="sxs-lookup"><span data-stu-id="32e5f-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-123">Il server ha negato la connessione.</span><span class="sxs-lookup"><span data-stu-id="32e5f-123">The server denied the connection.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span><span class="sxs-lookup"><span data-stu-id="32e5f-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-125">Il server ha negato la connessione per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="32e5f-125">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span><span class="sxs-lookup"><span data-stu-id="32e5f-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-127">Il server ha negato la connessione per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="32e5f-127">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span><span class="sxs-lookup"><span data-stu-id="32e5f-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-129">Sono necessarie credenziali aggiornate.</span><span class="sxs-lookup"><span data-stu-id="32e5f-129">Fresh credentials are required.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span><span class="sxs-lookup"><span data-stu-id="32e5f-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-131">La disconnessione è stata avviata dall'attività dell'utente.</span><span class="sxs-lookup"><span data-stu-id="32e5f-131">User activity has initiated the disconnect.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span><span class="sxs-lookup"><span data-stu-id="32e5f-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-133">L'utente si è disconnesso, disconnettendo la sessione.</span><span class="sxs-lookup"><span data-stu-id="32e5f-133">The user logged off, disconnecting the session.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span><span class="sxs-lookup"><span data-stu-id="32e5f-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-135">Errore interno di gestione licenze.</span><span class="sxs-lookup"><span data-stu-id="32e5f-135">Internal licensing error.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="32e5f-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-137">Nessun server licenze disponibile.</span><span class="sxs-lookup"><span data-stu-id="32e5f-137">No license server was available.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span><span class="sxs-lookup"><span data-stu-id="32e5f-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-139">Non è disponibile una licenza software valida.</span><span class="sxs-lookup"><span data-stu-id="32e5f-139">No valid software license was available.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span><span class="sxs-lookup"><span data-stu-id="32e5f-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-141">Il computer remoto ha ricevuto un messaggio di licenza non valido.</span><span class="sxs-lookup"><span data-stu-id="32e5f-141">The remote computer received a licensing message that was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span><span class="sxs-lookup"><span data-stu-id="32e5f-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-143">L'ID hardware non corrisponde a quello designato nella licenza software.</span><span class="sxs-lookup"><span data-stu-id="32e5f-143">The hardware ID does not match the one designated on the software license.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span><span class="sxs-lookup"><span data-stu-id="32e5f-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-145">Errore di licenza client.</span><span class="sxs-lookup"><span data-stu-id="32e5f-145">Client license error.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span><span class="sxs-lookup"><span data-stu-id="32e5f-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-147">Si sono verificati problemi di rete durante il protocollo di gestione licenze.</span><span class="sxs-lookup"><span data-stu-id="32e5f-147">Network problems occurred during the licensing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span><span class="sxs-lookup"><span data-stu-id="32e5f-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-149">Il client ha terminato il protocollo di gestione delle licenze in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="32e5f-149">The client ended the licensing protocol prematurely.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span><span class="sxs-lookup"><span data-stu-id="32e5f-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-151">Un messaggio di licenza è stato crittografato in modo errato.</span><span class="sxs-lookup"><span data-stu-id="32e5f-151">A licensing message was encrypted incorrectly.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span><span class="sxs-lookup"><span data-stu-id="32e5f-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-153">Non è stato possibile aggiornare o rinnovare la licenza di accesso client del computer locale.</span><span class="sxs-lookup"><span data-stu-id="32e5f-153">The local computer's client access license could not be upgraded or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span><span class="sxs-lookup"><span data-stu-id="32e5f-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-155">Il computer remoto non dispone della licenza per accettare le connessioni remote.</span><span class="sxs-lookup"><span data-stu-id="32e5f-155">The remote computer is not licensed to accept remote connections.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span><span class="sxs-lookup"><span data-stu-id="32e5f-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-157">È stato ricevuto un errore di accesso negato durante la creazione di una chiave del registro di sistema per l'archivio licenze.</span><span class="sxs-lookup"><span data-stu-id="32e5f-157">An access denied error was received while creating a registry key for the license store.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span><span class="sxs-lookup"><span data-stu-id="32e5f-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-159">Sono state rilevate credenziali non valide.</span><span class="sxs-lookup"><span data-stu-id="32e5f-159">Invalid credentials were encountered.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span><span class="sxs-lookup"><span data-stu-id="32e5f-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-161">Inizio dell'intervallo di errori interni del protocollo.</span><span class="sxs-lookup"><span data-stu-id="32e5f-161">Beginning the range of internal protocol errors.</span></span> <span data-ttu-id="32e5f-162">Per ulteriori informazioni, consultare il registro eventi del server.</span><span class="sxs-lookup"><span data-stu-id="32e5f-162">Check the server event log for additional details.</span></span>

</dd> <dt>

<span data-ttu-id="32e5f-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span><span class="sxs-lookup"><span data-stu-id="32e5f-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span></span>
</dt> <dd>

<span data-ttu-id="32e5f-164">Fine dell'intervallo di errori interni del protocollo.</span><span class="sxs-lookup"><span data-stu-id="32e5f-164">Ending the range of internal protocol errors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32e5f-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32e5f-165">Requirements</span></span>



| <span data-ttu-id="32e5f-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="32e5f-166">Requirement</span></span> | <span data-ttu-id="32e5f-167">Valore</span><span class="sxs-lookup"><span data-stu-id="32e5f-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32e5f-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32e5f-168">Minimum supported client</span></span><br/> | <span data-ttu-id="32e5f-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32e5f-169">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="32e5f-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32e5f-170">Minimum supported server</span></span><br/> | <span data-ttu-id="32e5f-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32e5f-171">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="32e5f-172">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="32e5f-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="32e5f-173"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32e5f-173"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e5f-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32e5f-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e5f-175">**ExtendedDisconnectReason**</span><span class="sxs-lookup"><span data-stu-id="32e5f-175">**ExtendedDisconnectReason**</span></span>](imsrdpclient-extendeddisconnectreason.md)
</dt> </dl>

 

 





